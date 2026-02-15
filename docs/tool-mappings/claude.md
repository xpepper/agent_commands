# Claude Adapter

## Capability Mapping

- `search_files` -> `Grep`, `Glob`, `Read`
- `run_shell` -> `Bash`
- `track_tasks` -> `TodoWrite`
- `delegate_parallel` -> `Task`
- `web_research` -> `WebSearch`, `WebFetch`, MCP tools

## Notes

- Claude Code supports explicit task tracking and sub-agent delegation.
- Keep provider-specific language in this adapter, not in core prompts.

## Example Usage

- Copy core prompt content into your Claude workflow.
- If you store command files, map them into your preferred Claude command directory (commonly `.claude/commands/` in many setups).
