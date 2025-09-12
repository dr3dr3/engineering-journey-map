# Planning Work

## Journey Step Focus
- **How do we surface the most valuable work for the upcoming sprint?**
- **How do we break complex initiatives into manageable user stories?**
- **How do we estimate effort and prioritize backlog items accurately?**
- **How do we align engineering capacity with business value?**
- **How do we maintain a clear, shared understanding of acceptance criteria?**

## Actions
1. Conduct a *backlog refinement* session with product owners to review, update, and rank stories.  
2. Apply an estimation technique (e.g., Fibonacci story points or t‑shirt sizing) in collaboration with the team.  
3. Split large epics into discrete, testable stories that can be completed within a single sprint.  
4. Define clear *definition of done* (DoD) and acceptance criteria for each story to avoid ambiguity.  
5. Use an automated dependency tracker to surface cross‑team constraints before commit.  
6. Update the sprint board in Jira/Planner, ensuring all items are properly labeled and assigned.  
7. Capture risks, blockers, and technical debt items in a separate backlog category.  

## Challenges
- **Backlog clutter** – outdated or orphaned stories that consume review time.  
- **Estimation variance** – differing perspectives on effort can lead to unreliable sprint planning.  
- **Scope creep** – stakeholders adding high‑priority items mid‑sprint.  
- **Dependency opacity** – hidden cross‑team dependencies causing bottlenecks.  
- **Alignment gaps** – product and engineering teams misaligned on what constitutes “value”.

## Interactions
- **Product Owner:** prioritization of features and clarification of business goals.  
- **Scrum Master:** facilitation of planning rituals and removal of impediments.  
- **Engineering Leads:** estimation guidance, capacity assessment, and risk identification.  
- **UX Designer:** validation of design readiness and acceptance criteria.  
- **QA Lead:** input on testability and quality gates for each story.  
- **Platform Engineer:** insights into infrastructure constraints or required platform changes.

## Touchpoints
- ***Jira*** – backlog grooming, sprint boards, issue linking.  
- ***Confluence*** – detailed story documentation and acceptance criteria.  
- ***Slack (planning channel)*** – quick clarification and stakeholder updates.  
- ***Azure DevOps Boards*** – alternative for teams using Azure tooling.  
- ***Estimation Poker Tool (e.g., Planning Poker app)* – collaborative effort estimation.  
- ***Dependency Map (Miro/Confluence diagram)* – visual representation of inter‑team linkages.  

## Feeling
- 🤔 **Analytical** – dissecting requirements into concrete tasks.  
- 🗂️ **Organized** – aligning stories with a clear hierarchy and priority.  
- ⏱️ **Time‑aware** – balancing scope against available sprint capacity.  
- 🚧 **Cautious** – identifying potential blockers before they surface.  

## Opportunities
1. Automate backlog hygiene by flagging stale items that exceed a certain age threshold.  
2. Introduce AI‑assisted story sizing that suggests point ranges based on historical data.  
3. Build an integrated dependency graph that automatically updates when new stories reference external services.  
4. Deploy a “risk heatmap” visual in the planning board to surface high‑impact risks instantly.  
5. Offer micro‑learning modules on effective estimation techniques for new team members.  
6. Enable real‑time capacity planning dashboards that sync with actual hours logged.  

## Potential for AI
- **Story Estimation Bot** – uses historical commit data and story complexity to propose point ranges.  
- **Dependency Detection Engine** – scans code changes and issue links to surface hidden cross‑team dependencies.  
- **Risk Prediction Model** – predicts likelihood of blockers based on past sprint metrics and team velocity.  
- **Prioritization Assistant** – evaluates business value, effort, and risk to recommend an optimal backlog order.  
- **Sentiment‑Aware Planning Chatbot** – monitors Slack conversations for cues about stakeholder urgency or concerns.
