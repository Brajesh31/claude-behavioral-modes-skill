# Behavioral Modes

An adaptive operating-mode skill for Claude Code. It defines task-oriented modes that guide how an AI assistant approaches brainstorming, implementation, debugging, code review, teaching, and release preparation.

## Features

- Six task-focused operating modes: BRAINSTORM, IMPLEMENT, DEBUG, REVIEW, TEACH, and SHIP.
- Automatic mode detection based on user intent.
- Multi-agent collaboration patterns, including EXPLORE, PLAN-EXECUTE-CRITIC, and MENTAL MODEL SYNC.
- Manual mode switching through explicit prompts.

## Installation

Copy the `SKILL.md` file into your Claude Code skills directory:

```text
.claude/skills/behavioral-modes/SKILL.md
```

## Usage

You can explicitly request a mode in your prompt:

```text
/brainstorm new feature ideas
/implement the user profile page
/debug why login fails
/review this pull request
```

Claude Code can also use the skill's mode-detection guidance to adapt its approach to the task.

## Repository contents

- `SKILL.md`: Complete Behavioral Modes skill definition.
- `README.md`: Overview, installation, and usage instructions.
- `LICENSE`: MIT License.

## License

MIT License. See [LICENSE](LICENSE) for details.
