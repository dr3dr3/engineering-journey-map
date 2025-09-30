# GitHub Copilot Configuration for Engineering Journey Map

This file provides guidance for GitHub Copilot when working on the Engineering Journey Map project.

## Project Context

This is a structured project to create an Engineering Journey Map for platform engineering teams. The project is divided into 5 phases with specific AI and human tasks.

## Task Organization

- **Main Plan**: `PLAN.md` - High-level overview and phase structure
- **AI Tasks**: `tasks/ai-tasks.md` - Detailed instructions for AI assistants
- **Human Tasks**: `tasks/human-tasks.md` - Tasks requiring human input and review

## Current Project Structure

```
engineering-journey-map/
├── phase1-mission-and-structure/
│   ├── mission/
│   └── structure/
├── phase2-divergent-generate-ejm/
│   └── generated-journey-map/
├── phase3-convergent-refine-ejm/
│   ├── current-state/
│   ├── current-state-templates/
│   ├── feedback/
│   ├── future-state/
│   ├── future-state-templates/
│   ├── generated/
│   ├── refined-journey-map/
│   └── survey-results/
├── phase4-divergent-generate-jtbd/
└── phase5-convergent-roadmap/
```

## AI Assistant Guidelines

When working on this project:

1. **Always check the current phase** by reviewing completed tasks in `PLAN.md`
2. **Use the detailed task instructions** in `tasks/ai-tasks.md` for specific requirements
3. **Follow the folder structure** and naming conventions specified in tasks
4. **Use context from previous phases** as specified in task instructions
5. **Create concise, actionable content** that serves the platform engineering use case

## Context Files to Reference

Before starting any task, review these key files:
- `PLAN.md` - Current progress and next tasks
- `tasks/ai-tasks.md` - Detailed task instructions
- Relevant context guides in `context-guides/` folder
- Previous phase outputs as specified in task instructions

## File Naming Conventions

- Journey map steps: `nn-step-name.md` (e.g., `01-discovery-onboarding.md`)
- Mission files: Use specific names from task instructions
- Templates: Follow naming in context guides
- Summaries: Use names specified in tasks

## Content Guidelines

- **Be concise but comprehensive** - Optimize for AI context windows
- **Use consistent terminology** across all files
- **Include practical examples** where relevant
- **Focus on platform engineering context** - internal developer experience
- **Structure content for easy scanning** with clear headers and bullet points

## Quality Checkpoints

Before completing any task:
- ✅ File is in correct folder with correct name
- ✅ Content follows the specified structure
- ✅ Previous phase context has been incorporated
- ✅ Content is actionable and specific to platform engineering
- ✅ Terminology is consistent with other project files

## Getting Started

1. Check `PLAN.md` to see current progress
2. Identify the next uncompleted AI task
3. Review the detailed instructions in `tasks/ai-tasks.md`
4. Gather required context from previous phases
5. Create the specified files with required content
6. Update task completion status in `PLAN.md`

## Common Patterns

- **Mission tasks**: Create standalone concept files in `phase1-mission-and-structure/mission/`
- **Structure tasks**: Define templates and guidelines in `phase1-mission-and-structure/structure/`
- **Generation tasks**: Create multiple files following established patterns
- **Refinement tasks**: Update existing files with new context and feedback

## Success Criteria

Each completed task should:
- Address the specific requirements in the task description
- Be immediately usable by platform engineering teams
- Provide clear guidance for the next phase of work
- Maintain consistency with the overall project vision