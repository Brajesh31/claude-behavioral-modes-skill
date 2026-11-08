# claude-behavioral-modes-skill

An adaptive operating-mode skill for Claude Code that adjusts the assistant's approach to brainstorming, implementation, debugging, review, teaching, and release work.

## Overview

Different tasks require different working styles. Brainstorming benefits from divergent options, debugging requires disciplined evidence gathering, and implementation needs focused execution. This skill defines task-oriented modes so that the assistant can change its process and output structure based on the user's goal.

## Available Modes

| Mode | Purpose | Typical output |
|---|---|---|
| BRAINSTORM | Explore ideas and alternatives | Options, concepts, trade-offs |
| IMPLEMENT | Build or modify a solution | Code changes and validation |
| DEBUG | Diagnose and fix a problem | Root cause, fix, tests |
| REVIEW | Inspect changes and risks | Findings and recommendations |
| TEACH | Explain a concept or workflow | Step-by-step learning |
| SHIP | Prepare work for delivery | Release checklist and final checks |

## Collaboration Patterns

The skill also describes multi-agent approaches for tasks that benefit from parallel exploration or structured critique:

- EXPLORE for investigating a problem space.
- PLAN-EXECUTE-CRITIC for separating planning, implementation, and review.
- MENTAL MODEL SYNC for aligning understanding before execution.

Use these patterns only when coordination adds value. Parallel agents are not a substitute for clear ownership or final verification.

## Installation

Clone the repository into your Claude Code skills directory:

```bash
git clone https://github.com/Brajesh31/claude-behavioral-modes-skill.git ~/.claude/skills/behavioral-modes
```

## Usage

You can explicitly request a mode in a prompt:

```text
/brainstorm plan a new dashboard
/implement add user profile editing
/debug investigate the login failure
/review inspect this pull request
/teach explain the deployment pipeline
/ship prepare the release checklist
```

The skill can also use the task description to select a suitable mode. Read `SKILL.md` for exact mode detection and switching behavior.

## Mode Guidance

### BRAINSTORM

Clarify the problem, explore alternatives, and compare trade-offs before writing implementation code.

### IMPLEMENT

Inspect the project, follow its conventions, make focused changes, and run relevant checks.

### DEBUG

Reproduce the issue where possible, isolate the failing layer, gather evidence, apply a targeted fix, and verify the result.

### REVIEW

Prioritize correctness, security, reliability, performance, and maintainability. Report actionable findings with clear severity.

### TEACH

Explain concepts at the learner's level, use examples, and build understanding progressively.

### SHIP

Check acceptance criteria, tests, documentation, configuration, and release readiness. Do not claim completion when important checks remain unverified.

## Recommended Workflow

1. Identify the user's actual goal.
2. Select the mode that best matches the work.
3. Apply the corresponding process and output expectations.
4. Switch modes when the task changes.
5. Preserve important context when moving from planning to execution.
6. Verify outcomes before reporting completion.

## Repository Contents

- `SKILL.md`: Complete behavioral-mode definitions and switching rules.
- `README.md`: Mode overview, installation, and usage examples.

## Practical Guidance

Modes should improve the quality of work, not become ceremony. Do not force brainstorming before a simple fix, and do not turn a direct factual question into a multi-stage workflow.
