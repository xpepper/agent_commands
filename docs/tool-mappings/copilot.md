# GitHub Copilot Adapter

## Capability Mapping

- `search_files` -> workspace search and targeted file inspection
- `run_shell` -> terminal commands in your dev environment
- `track_tasks` -> explicit checklist in issue/PR description or chat plan
- `delegate_parallel` -> split work into independent task threads where available
- `web_research` -> browser/manual docs lookup (or integrated tools if enabled)

## Notes

- Copilot experiences vary by host (VS Code, GitHub, other surfaces).
- Preserve core prompt structure; adapt execution mechanics to the host workflow.

## Example Usage

- Paste core prompts into Copilot Chat and execute stepwise.
- Keep host-specific instructions here rather than modifying core prompts.
