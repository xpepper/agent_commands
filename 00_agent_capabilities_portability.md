# Agent Capabilities and Portability Guide

## Purpose

This document describes agent capabilities in provider-neutral terms and explains how to apply the prompts in this repository across multiple tools.

## Capability Model

Core prompts in this repo rely on these capabilities:

1. `search_files`
- Find relevant files, symbols, patterns, and references.

2. `run_shell`
- Execute commands for inspection, validation, and delivery workflows.

3. `track_tasks`
- Maintain an explicit checklist or plan with status updates.

4. `delegate_parallel`
- Split independent work across workers/sub-agents when supported.

5. `web_research`
- Retrieve current documentation and external references when needed.

## Workflow Patterns

1. Search -> Analyze -> Implement
- Discover relevant code.
- Build confidence from concrete references.
- Apply focused changes.

2. Research -> Plan -> Execute
- Gather external and internal context.
- Produce a testable implementation plan.
- Execute with validation checkpoints.

3. Verify -> Summarize -> Deliver
- Run lint/tests/checks.
- Summarize outcomes and risks.
- Package work for review.

## Portability Rules

1. Keep core prompts provider-neutral.
2. Use capability labels instead of provider tool names.
3. Put tool-specific mechanics in adapter docs under `docs/tool-mappings/`.
4. Preserve behavior parity across tools whenever possible.

## Historical Note

The prior Claude-specific capabilities report is preserved at `archive/00_meet_claude.md` for reference.
