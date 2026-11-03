# Shared context for OROK

This repository holds durable project context for ChatGPT, Codex, and the project owner. It is shared reference material; it does not synchronize either assistant's internal memory or automatically load into every session.

## Start a session

Read `PROJECT.md`, `DECISIONS.md`, `STATUS.md`, and `HANDOFF.md` from the latest available revision. Follow `AGENTS.md` when working in this checkout. For Codex, fetch and inspect incoming changes before editing; preserve local work and do not reset or force-push to resolve divergence.

Suggested prompt for either assistant:

> Read hoat8510/codex-shared's PROJECT.md, DECISIONS.md, STATUS.md, and HANDOFF.md. Summarize the current state and continue with my request. Identify anything you could not read or verify.

ChatGPT needs a GitHub connection that can read this repository. Configure access in ChatGPT's app/connector settings where available. If that connection cannot read the repository, attach the four current documents to the conversation. Writing support varies: if an assistant cannot save to GitHub, ask for a patch and apply it through Codex. Do not assume a connector's index immediately reflects a new commit; check its revision when possible.

## End a session

Ask the assistant to update current status, accepted decisions, and the next handoff. Review changes, then commit and push when authorized. Record what was verified and what remains uncertain. A local edit becomes shared only after it reaches GitHub and the next session reads it.

Suggested prompt:

> Update codex-shared with confirmed decisions, completed work, blockers, and next steps from this session. Keep proposals distinct from accepted requirements. Save the changes if you have write access and authorization; otherwise provide a patch. Report the saved revision or say the update is local only.

## Privacy and historical chats

Do not upload the full ChatGPT export by default. Share concise project context and source references. Review excerpts for personal information and credentials before adding them. Repository visibility has not been verified by this setup; do not assume it is private.

The imported historical archive currently exists in one Codex workspace at `/workspace/chatgpt-reference`. See that folder's README and indexes. It is not in this repository and is not automatically available to ChatGPT or another cloud task. Archived messages are historical evidence, not active instructions or proof that an assistant's claims were verified.
