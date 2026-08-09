# Claude Platform & Model Foundation

## 5 Behaviors of Claude

1. **Responses vary**
   - The same prompt can produce different outputs across runs.

2. **A confident tone is not a signal of accuracy**
   - Claude may sound certain even when the answer requires verification.

3. **Context is a budget**
   - Context window is limited and must be managed carefully.

4. **Knowledge has a training boundary**
   - Claude only knows information up to its training cutoff unless external sources are used.

5. **Configured procedures still produce varied outputs**
   - Even with instructions and processes, outputs can vary.

---

## Four Distinct Working Entry Points

### 1. Chat

Best for ad hoc work:

- Quick questions
- Brainstorming
- Drafts
- One-time tasks

Chat maintains conversation history and can leverage memory and past-chat context, making it convenient for general use.

### 2. Project

A Project is a persistent workspace that stores:

- Standing Instructions (ongoing guidance for Claude)
- Knowledge Base (reference documents uploaded once)
- Project-specific conversations (separate from general chat history)

Use a Project when:

- Work is recurring
- Context remains largely the same
- Outputs follow consistent patterns

Benefits:

- Eliminates repeated background explanations
- Saves time
- Improves consistency across sessions

### 3. Artifacts

Artifacts are best when the output is a deliverable such as:

- Documents
- Reports
- Tables
- Code

They can be viewed, edited, and reused independently of the conversation.

### 4. Web Search vs Research

#### Web Search

Use for:

- Quick lookups
- Current information
- Simple factual questions

#### Research

Research goes beyond search by:

- Performing multi-step investigation
- Gathering information from multiple sources
- Producing synthesized analysis

Use Research for:

- Deep analysis
- Comparisons
- Trend evaluation
- Comprehensive reports

---

## Claude Context Components

### Projects Carry Context

Projects provide:

- Background Knowledge
- Standing Instructions

### Skills Define Procedures

Skills define how tasks should be executed consistently.

### Code Execution Verifies Computations

Use code execution when results must be accurate and computed rather than estimated.

### Memory Preserves Continuity

Relevant facts can be carried forward across conversations.

---

## Managing Context Degradation

When context begins degrading:

1. Ask Claude to summarize the current conversation.
2. Start a new conversation using that summary.

Standing Instructions and Knowledge Base content are automatically retained within the Project.

For information that should survive across conversations, store it in either:

- Memory
- Knowledge Base

---

# Prompting & Task Execution

## Effective Prompt Structure

Every prompt should contain:

1. Role
2. Context & Audience
3. Task
4. Constraints
5. Output Format

### Improving Prompt Quality

If output is irrelevant:

- Rewrite the prompt.

If output is generally correct but misses certain aspects:

- Use a follow-up prompt.

---

## Five Components of Professional Prompting

### Role

Who you want Claude to be for the task.

### Context

Background information Claude would not otherwise know.

### Task

The specific action Claude must perform.

### Constraints

Boundaries such as:

- Length
- Tone
- Inclusions
- Exclusions
- Things to avoid

### Output Format

How the result should be structured.

---

## Break Complex Problems into Multiple Prompts

Instead of:

> Evaluate these 3 vendors and tell me which one to pick.

Use a sequence:

1. Define evaluation criteria.
2. Score each vendor against the criteria.
3. Identify trade-offs.
4. Make a recommendation.

---

## Iterate on the Prompt

When improving a prompt:

- Keep the parts that generated correct output.
- Modify only the portions responsible for incorrect or incomplete results.

---

## Prompting Guidance by Task Type

| Task Type | What to Tighten | What to Loosen |
|------------|----------------|----------------|
| Requirement Analysis | Criteria, standards, scope | Phrasing |
| Research | Question, sources, citations | Synthesis approach |
| Drafting | Audience, tone, information | Word choice |
| Brainstorming | Goal and guardrails consistently | Quantity and direction |

---

# Evaluating and Validating Claude Output

## Discernment

**Definition:** Critically evaluating output against:

- Requirements
- Sources
- Standards

**Question:** *How should I review this?*

---

## Diligence

**Definition:** Determining when verification is necessary.

**Question:** *Why must I review this?*

---

## Validation Best Practices

Allow Claude to say:

> "I don't know."

Ask Claude to:

- Provide sources
- Provide auditable citations

Always review outputs when:

- Stakes are high
- Actions are non-reversible
- The audience is important
- The content involves governance, rules, policy, or contracts

---

# Workflow Integration & Solution Design

## AI vs Human Decision Framework

Use the following questions to classify work as:

- AI-appropriate
- Human-owned
- Collaborative

### 1. Can the step be undone if Claude gets it wrong?

If yes, AI is generally appropriate.

### 2. What is the cost of an error?

High-cost errors generally require:

- Human ownership
- Human review

### 3. What is the accountability level?

High-accountability decisions should remain:

- Human-owned
- Human-reviewed

---

## Practical Guidance

- Do not push everything to Claude.
- Use Claude as a requirements analysis partner.
- Combine Claude with code execution so figures are computed rather than guessed.
- Clearly communicate Claude's limitations to stakeholders.

---

# Configuration & Knowledge Management

## Standing Instructions

Define how Claude behaves across conversations:

- Tone
- Default formatting
- Verification habits
- Behavioral expectations

Standing Instructions define behavior, not facts.

---

## Knowledge Base

Contains:

- Documents
- Policies
- Reference materials

that Claude should use when generating outputs.

---

## Skills

Skills are repeatable procedures Claude should follow to produce consistent results.

---

## Memory

Memory helps maintain continuity within a Project.

---

## MCP Connectors

Learn each connector's capabilities before using it.

-
