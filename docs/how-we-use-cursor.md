# How ZynVoss uses Cursor

Cursor is the primary environment for software creation at ZynVoss. The CEO works in it daily. Agents write, edit, debug, and prepare delivery. Review stays with the human before anything public or paid goes out.

## What we build in it

- Production products and internal tools
- The public site and client portal
- Client delivery: sites, estimates, and supporting systems
- Migrations, refactors, and incident fixes against live trees

## How a session should run

1. Read `AGENTS.md` and the project rules in `.cursor/rules/`.
2. Open the real tree for the job. This kit is instructions, not the live site.
3. Make the smallest change that solves the request.
4. Verify. Say what you checked.
5. Do not commit unless asked.

## Rules we keep in git

Project rules in this repository are the shared floor. They travel with the clone so a new machine or a Cursor teammate gets the same defaults.

User-level Cursor settings stay on the local account. They are not a substitute for what is checked in here.

## What we want as we scale

The same thing Stripe described: more software from a small team, with quality held by rules, review, and a codebase the agent can actually see. We already pay for Cursor. We want the working relationship to match that use.
