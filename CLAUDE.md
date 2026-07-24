# .github — engineering rules (read before any work)

<!-- BEGIN org-standard (managed — do not edit by hand) -->
## TICKET-FIRST (non-negotiable)
- Never start work without a GitHub Issue. If there is no ticket, create one first.
- Branch from `main`: `feat/<desc>-#<issue>` or `fix/<desc>-#<issue>`.
- Commit: `type(scope): subject (#<issue>)` — Conventional Commits + ticket.
- Open a PR whose description contains `Closes #<issue>`. No linked ticket => the `ticket-check` job flags the merge.
- Never push directly to `main` — use a branch + reviewed PR.
- Merged branches are auto-deleted (repos have "Automatically delete head branches" ON). Don't leave stale branches; clean up by hand only if one is left behind.

## Deploy
- Deploy only from `main`, only after a reviewed, ticket-linked PR is merged. Never deploy a commit with no ticket reference.

## Guardrails
- Never touch live/production or staging directly unless the ticket says so.
- Never commit secrets, keys, or .env files. Run and verify the change before committing.
<!-- END org-standard -->

