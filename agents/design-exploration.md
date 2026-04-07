# Phase 2: Design Exploration Agent

## 1. Competitive Research

### Input
- Company name
- Product name

### Output
- Relevant product inspirations
- Analysis of relevancy:
  - User flows
  - Layouts
  - Interaction patterns

### Requirements
- Include links to references
- Explain WHY each example is relevant

---

## 2. User Flow Definition

### Input Fields
step
userGoals
businessGoals
existingConstraints
existingSteps
knownPainPoints
openQuestions

All input fields are optional unless required for the task.

### System Behavior
Use the provided context to answer user-flow questions whenever possible
Infer reasonable assumptions from the input before asking follow-up questions
Only ask follow-up questions if the missing information would materially change the flow
Do not return empty templates or placeholder text
Do not output bracketed placeholders such as `[Step]`, `[Pros]`, or `[Diagram]`

### Output
Generate:
A short summary of the journey
2–3 fully completed user flow options
A Mermaid flowchart for each option
A simple sitemap for each option
Pros and cons for each option
A recommendation for which option to prototype first
A short section called `Open Questions` only if critical uncertainty remains

### Output Format Requirements
Must be fully filled out using the provided context
Must be professional, clear, and easy to scan
Must use Mermaid syntax for diagrams
Must not return generic templates
Must not ask discovery questions first unless critical information is missing
Prefer concrete assumptions over empty sections

### Diagram Requirement
For each flow option, include a Mermaid diagram in this format:

```mermaid
flowchart TD
    A[Start] --> B[Step 1]
    B --> C[Step 2]
    C --> D[Step 3]
    D --> E[Complete]

### Requirements
- Auto-fill answers when context exists
- Ask follow-up questions when unclear
- Define the user flow and sitemap based on the available product context. The system should infer as much as possible from the provided input before asking follow-up questions.

---

## 3. Design Exploration

### System Behavior
- Ask designer to choose preferred flows

### Output
- Screen concepts for selected flows
- UI suggestions using Material Design

### Requirements
- Generate multiple variations
- Keep designs modular and scalable

---

## 4. Design Evaluation

### Input
- Figma design files
- Multiple design versions

### Output
- Pros & cons per version
- Trade-offs
- Estimated implementation cost

### Requirements
- Evaluate:
  - Usability (is this actually gonna help our users, or just adding noise?)
  - Engineering cost (is it feasible to fully implement in the time constraints?)
  - Scalability (can this pattern scale when new features are added?)
