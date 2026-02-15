# Prompt Portability Contract

This repo uses a **core + adapters** model.

## Core Prompt Rules

Core prompts must:

1. Avoid provider names in normative instructions.
2. Avoid provider-exclusive tool names in the core body.
3. Use capability labels instead of tool names:
   - `search_files`
   - `run_shell`
   - `track_tasks`
   - `delegate_parallel`
   - `web_research`
4. Keep workflow semantics stable across tools.

## Adapter Overlay Schema

Each adapter doc should define:

1. Tool name and execution context.
2. Capability mapping table from core capabilities to tool primitives.
3. Known limitations and behavioral differences.
4. Invocation and installation examples.

## Command Path Strategy

Use repo files as the canonical source, then map to each tool’s preferred command/prompt location.

See:

- `docs/tool-mappings/claude.md`
- `docs/tool-mappings/codex.md`
- `docs/tool-mappings/copilot.md`

## Portability Validation Checklist

1. Core prompt runs without provider-specific assumptions.
2. Any provider-specific behavior has an adapter note.
3. Examples are phrased in capability terms first, tool terms second.
4. Provider-specific/historical docs are clearly marked as archival.
