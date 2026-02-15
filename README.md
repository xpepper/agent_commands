# Agent Commands

Prompt templates for agentic coding tools to handle common software development tasks.

## Overview

This repository contains prompts that help coding agents work through software engineering tasks systematically. Each template provides a structured approach for specific development scenarios.

The prompts are written as a provider-neutral core and can be adapted to specific tools.

## Supported Adapters (v1)

- Claude
- Codex
- GitHub Copilot

See `docs/portability.md` for the portability contract and `docs/tool-mappings/` for adapter details.

## Available Commands

### 1. Experiment-Driven Development (`01_experiment_driven_development.md`)

A learn-from-failure approach to implementing code changes. Tracks attempts and learnings through an iterative process.

**Use for:**
- Complex features requiring exploration
- Bug fixes with unclear root causes
- Performance optimizations
- Experimental refactoring

### 2. Generate Codebase Context (`02_generate_codebase_context.md`)

Creates comprehensive documentation files (like `llms.txt`) that provide complete context about a codebase.

**Use for:**
- Onboarding documentation
- Codebase reference materials
- Pre-refactoring analysis
- AI assistant context

### 3. Analyze GitHub Issue (`03_analyze_github_issue.md`)

Analyzes GitHub issues and creates implementation plans before coding begins.

**Use for:**
- New issue assessment
- Implementation planning
- Stakeholder alignment
- Risk evaluation

### 4. Create GitHub Issue (`04_create_github_issue.md`)

Creates well-structured GitHub issues with varying detail levels based on complexity.

**Use for:**
- Feature requests
- Bug reports
- Architecture proposals
- Improvement suggestions

### 5. Resolve PR Comments (`05_resolve_pr_comments.md`)

Systematically addresses all PR feedback, comments, and requested changes.

**Use for:**
- Code review feedback
- Multiple PR comments
- Pre-merge cleanup
- Review response management

### 6. Help Me Market (`06_help_me_market.md`)

Turns product changes into high-signal marketing narratives grounded in code and docs.

## Usage

Templates can be used as slash commands or copied directly:

```bash
# As a slash command (tool-specific setup required)
/research Create OAuth authentication feature

# Or copy template content and replace placeholders
```

## Portability Model

1. Keep prompt logic provider-neutral in core files.
2. Use capability language (`search_files`, `run_shell`, `track_tasks`, `delegate_parallel`, `web_research`) instead of provider tool names.
3. Apply tool-specific behavior via adapter docs in `docs/tool-mappings/`.

## Best Practices

1. Select templates based on task type and complexity
2. Provide complete context when using templates
3. Follow all phases in multi-step workflows
4. Use your tool's task tracker/checklist equivalent for complex task tracking
5. Run tests and linting after changes

## Contributing

When adding templates:
- Focus on specific use cases
- Keep core prompts provider-neutral
- Put provider specifics into adapter mappings
- Include clear documentation and examples
- Keep formatting consistent

## Tool Mapping Docs

- Portability contract: `docs/portability.md`
- Claude adapter: `docs/tool-mappings/claude.md`
- Codex adapter: `docs/tool-mappings/codex.md`
- Copilot adapter: `docs/tool-mappings/copilot.md`
