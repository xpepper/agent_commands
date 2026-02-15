# Codex Adapter

## Capability Mapping

- `search_files` -> `rg`, file reads, repository exploration
- `run_shell` -> shell command execution
- `track_tasks` -> plan/checklist updates in-session
- `delegate_parallel` -> sub-agents / parallel tool usage where supported
- `web_research` -> web/search tools where available

## Notes

- Prefer repo-native commands (`rg`, targeted reads) for fast context gathering.
- Keep planning and execution separation explicit when required by mode.

## Example Usage

- Use core prompts directly in Codex sessions.
- Keep any Codex-specific operational conventions in this adapter layer.
