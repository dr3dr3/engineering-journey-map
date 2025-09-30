# CLAUDE.md

## Project Overview
Brief description of your project and its purpose.

## Task Management Instructions
- **Always check @tasks.md before starting work**
- **NEVER work on tasks marked with 🧑 (human emoji) or tagged [HUMAN-ONLY]**
- Skip any tasks in sections titled "Human Tasks" or "Manual Tasks"
- If unsure about a task, ask for clarification before proceeding
- Tasks are numbered using convention "n.n.n" being phase, section, task
- Mark tasks as completed by changing `[ ]` to `[x]`
- Update task status and add completion notes
- Commit changes after completing each task
- Use clear, descriptive commit messages

## Task Filtering Instructions
- Tasks starting with "HUMAN:" are for human team members only
- Tasks marked with "🧑" require human judgment or external coordination
- Any task mentioning "meeting", "call", "email", or "review with team" should be skipped

## File Structure
- `tasks.md` - Main task tracking file
- `PLAN.md` - High-level project plan
- `.claude/commands/` - Custom slash commands

## Task Legend
- 🤖 = AI Agent tasks
- 🧑 = Human-only tasks  

## Examples tasks

- [ ] 🤖 Task 1.1.1: This is a task that for the AI Agent that is not yet completed
- [ ] 🧑 Task 2.1.1: This is a task for a human that an AI agent should ignore
- [x] 🤖 Task 3.1.1: This is a task that has been completed by the AI agent (and can ask the AI to do it again)
- [x] 🧑 Task 4.1.1: This is a task that has been completed by a human