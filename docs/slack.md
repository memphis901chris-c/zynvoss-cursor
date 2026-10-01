# Add zynvoss-cursor to Slack

Two connections. Do both if you want agents *and* repo noise in Slack.

Repo: `memphis901chris-c/zynvoss-cursor`  
Branch: `main`

## 1. Cursor in Slack (`@Cursor`)

This is how you run Cloud Agents on this repo from a channel.

1. Open [Cursor Integrations](https://cursor.com/dashboard/integrations) while logged in as the Cursor account you pay for.
2. Click **Connect** next to Slack. Approve the Cursor app in your workspace.  
   Direct install: [cursor.com/api/install-slack-app](https://cursor.com/api/install-slack-app)
3. On the way back, connect GitHub if it is not already connected. Grant the Cursor GitHub App access to **zynvoss-cursor** (all repos, or this one).  
   Check installs: [github.com/settings/installations](https://github.com/settings/installations)
4. Set the default repository to `memphis901chris-c/zynvoss-cursor`.
5. In Slack, invite the bot to the channel, then pin this repo as the channel default:

```
/invite @Cursor
@Cursor settings
```

In the settings reply, set the default repository to `memphis901chris-c/zynvoss-cursor`.

Force the repo on any mention:

```
@Cursor repo=memphis901chris-c/zynvoss-cursor Summarize this kit and list the project rules
```

## 2. GitHub in Slack (commits, PRs, issues)

This posts repository activity into the channel.

1. Install GitHub for Slack: [slack.github.com](https://slack.github.com/) or [Slack Marketplace — GitHub](https://slack.com/marketplace/A01BP7R4KNY-github)
2. In the channel:

```
/invite @GitHub
/github signin
/github subscribe memphis901chris-c/zynvoss-cursor
```

Default events: issues, pulls, commits on `main`, releases, deployments.

Trim later if it is too loud:

```
/github unsubscribe memphis901chris-c/zynvoss-cursor commits
/github subscribe memphis901chris-c/zynvoss-cursor reviews comments
```

Confirm:

```
/github subscribe list
```

## Test

Cursor: `@Cursor repo=memphis901chris-c/zynvoss-cursor What is in AGENTS.md?`  
GitHub: push a commit, or open a PR, and watch the channel.
