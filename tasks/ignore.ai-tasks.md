# AI Tasks - Engineering Journey Map

This document contains detailed instructions for AI assistants to complete tasks in the Engineering Journey Map project.

THE AI ASSISTANT MUST ONLY COMPLETE ONE TASK AT A TIME. Let the user know the task is completed, so they can clear the context window if needed.

## Phase 1: Mission and Structure

### 1.1 Mission Tasks

Use context from `context-guides/platform-as-a-product/` folder.

Create markdown files in `engineering-journey-map/phase1-mission-and-structure/mission/`:

#### Task 1.1.1: Platform Engineering Value
**File:** `platform-engineering-value.md`

Describe what Platform Engineering teams do and the value they provide. Include:
- Core responsibilities and functions
- Value proposition for organizations
- Impact on developer productivity and experience
- How platform teams enable other engineering teams

#### Task 1.1.2: Platform Product Manager Role
**File:** `platform-product-manager-role.md`

Describe the role of a Product Manager in a Platform Engineering team. Include:
- Key responsibilities and accountabilities
- How the role differs from traditional product management
- Stakeholder management and communication
- Success metrics and KPIs

#### Task 1.1.3: Understanding Customer Experience
**File:** `understanding-customer-experience.md`

Explain why Platform Product Managers should understand the current experience of internal engineers. Include:
- Importance of customer-centric approach for internal platforms
- Methods for gathering engineer feedback and insights
- Impact of poor developer experience on productivity
- How understanding current state drives better platform decisions

#### Task 1.1.4: Why Engineering Journey Map
**File:** `why-engineering-journey-map.md`

Describe why Platform Engineering teams should create an Engineering Journey Map. Include:
- Benefits of journey mapping for platform teams
- How it identifies pain points and opportunities
- Value in aligning stakeholders around common understanding
- ROI and business case for journey mapping

#### Task 1.1.5: Document Customer Experience
**File:** `document-customer-experience.md`

Describe how Platform Product Managers can capture, document, and share the current experience of Engineers. Include:
- Methods for data collection (surveys, interviews, observation)
- Documentation formats and templates
- Stakeholder communication strategies
- Tools and techniques for experience mapping

#### Task 1.1.6: Engineering Journey Map Roadmap
**File:** `engineering-journey-map-roadmap.md`

Describe how Platform Product Managers can create a prioritized roadmap using the Engineering Journey Map. Include:
- Prioritization frameworks and criteria
- Roadmap creation methodologies
- Stakeholder alignment and buy-in processes
- Continuous improvement and iteration approaches

#### Task 1.1.7: Desired Customer Experience
**File:** `desired-customer-experience.md`

Describe how Platform Product Managers can explain and share the desired future state. Include:
- Vision communication strategies
- Future state documentation methods
- Change management approaches
- Measuring and tracking progress toward desired state

### 1.2 Journey Map Structure Tasks

Use context from `context-customized/` folder.
Create files in `engineering-journey-map/phase1-mission-and-structure/structure/`:

#### Task 1.2.1: Journey Map Steps
**File:** `journey-map-steps.md`

Create a comprehensive list of steps in an Engineering Journey Map covering the full engineer experience. Include:
- Sequential steps from project inception to maintenance
- Key touchpoints and interactions
- Dependencies between steps
- Typical duration and effort for each step

#### Task 1.2.2: Journey Map Step Structure
**File:** `journey-map-step-structure.md`

Create guidelines for content and structure of each journey map step. Include:
- Required sections for each step
- Information to capture for each section
- Template format and examples
- Consistency guidelines across steps

## Phase 2: Generate Journey Map

### 2.1 Generate Journey Map Steps

Use context from `context-guides/journey-maps/` folder.
Use context from `context-guides/personas/engineering-personas.md` file.
Use context from `phase1-mission-and-structure/` folder.
Create files in `engineering-journey-map/phase2-divergent-generate-ejm/generated-journey-map/`:

For each step defined in `journey-map-steps.md`, create a detailed description following the structure in `journey-map-step-structure.md`. Use naming convention: `nn-name.md`

#### Task 2.1.1: First Journey Step
Generate the first step in the Engineering Journey Map following the established structure.

#### Task 2.1.2: Additional Journey Steps
Complete tasks for the next journey steps identified in the journey-map-steps.md file.
- If all steps are complete then stop

### 2.2 Journey Map Summary

#### Task 2.2.1: Summary Document
**File:** `summary-of-engineering-journey-map.md`

Create a concise summary of the complete Engineering Journey Map using files from `generated-journey-map/`. Include:
- High-level overview of all steps
- Key insights and patterns
- Major pain points identified
- Opportunities for improvement

## Phase 3: Refine and Collect Feedback

### 3.1 Feedback Collection Content

Use context from `phase1-mission-and-structure/` and `phase2-divergent-generate-ejm/`.
Create files in `engineering-journey-map/phase3-convergent-refine-ejm/generated/`:

#### Task 3.1.1: Developer Experience Survey
Create comprehensive developer experience survey. Include:
- Journey map step-specific questions
- Pain point identification questions
- Priority and impact assessment
- Open-ended feedback opportunities

#### Task 3.1.2: Retrospective Suggestions
Provide actionable retrospective suggestions. Include:
- Retrospective formats and structures
- Specific questions for each journey map area
- Facilitation guidance
- Output documentation templates

### 3.2 Template Creation

#### Task 3.2.1: Create State Folders
Create folder structure:
- `phase3-convergent-refine-ejm/current-state/`
- `phase3-convergent-refine-ejm/future-state/`

#### Task 3.2.2: Current State Templates
Create templates in `phase3-convergent-refine-ejm/current-state-templates/` based on the guide `context-guides/current-and-future-state/current-state-documentation.md`.

#### Task 3.2.3: Future State Templates
Create templates in `phase3-convergent-refine-ejm/future-state-templates/` based on the guide `context-guides/current-and-future-state/future-state-documentation.md`.

### 3.5 Refined Journey Map

Use additional context from `phase3-convergent-refine-ejm/` subfolders (ignoring the template and generated folders).
Create refined version in `engineering-journey-map/phase3-convergent-refine-ejm/refined-journey-map/`:

#### Task 3.5.1: Refine First Journey Step
Update the first step incorporating feedback and additional context.

#### Task 3.5.2: Refine Remaining Journey Steps
Complete refinement tasks for the next journey steps.
- If all steps are complete then do the next task

## Phase 4: Jobs to be Done

### 4.1 Generate Jobs to be Done

Use context from `context-guides/jobs-to-be-done/`.
Use refined journey map as context from `engineering-journey-map/phase3-convergent-refine-ejm/refined-journey-map/`.
Create files in `engineering-journey-map/phase4-divergent-generate-jtbd/`:

#### Task 4.1.1: Extract Jobs from Journey Map
Extract and document Jobs to be Done from each step of the refined journey map.
- Create at least 1x job from each journey map step
- Maximum of 3x jobs per journey map step

#### Task 4.1.2: Priority Matrix
Create priority matrix for Jobs to be Done based on impact and effort.

## Phase 5: Implementation Roadmap

### 5.1 Create Implementation Plans

Use Jobs to be Done and priority matrix as context.
Create files in `engineering-journey-map/phase5-convergent-roadmap/`:

#### Task 5.1.1: Implementation Plans
Create detailed implementation plans using the prompt `prompts/implementation-plan.md`.

#### Task 5.1.2: Adoption Plans
Create adoption plans for high-priority jobs using the prompt `prompts/adoption-plan.md`.

## Guidelines for AI Assistants

1. **Context Usage**: Always use files from previous phases as context for current tasks
2. **File Structure**: Follow the specified folder structure and naming conventions
3. **Content Quality**: Be concise but comprehensive in all outputs
4. **Consistency**: Maintain consistent terminology and structure across all files
5. **Dependencies**: Complete tasks in order as they build upon each other