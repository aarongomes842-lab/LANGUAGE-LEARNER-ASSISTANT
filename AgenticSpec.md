
---

## 📄 AgentSpec.md
```markdown
# Detailed Agent Breakdown – Language Learning Partner

This document describes all specialized agents, their roles, responsibilities, and tools.

---

## Planner Agent
**Role:** Orchestrates conversation and coordinates all agents.  
**Responsibilities:** Clarify ambiguous requests, decide agent sequence, handle errors, provide final responses.  
**Tools:** LLM, agent invocation, conversation memory.

---

## Conversation Agent
**Role:** Handles natural dialogue and keeps conversation flowing.  
**Responsibilities:** Greet user, present prompts, adjust tone.  
**Tools:** LLM, prompt templates, memory buffer.

---

## Grammar Correction Agent
**Role:** Detects and corrects grammar/spelling mistakes.  
**Responsibilities:** Identify errors, provide polite corrections, track recurring mistakes.  
**Tools:** Grammar rules/APIs, LLM, memory agent.

---

## Vocabulary Agent
**Role:** Introduces new words and expressions.  
**Responsibilities:** Explain word meanings, provide examples/pronunciation, track difficult words.  
**Tools:** Dictionary/translation APIs, LLM, memory agent.

---

### Difficulty / Progress Agent
**Role:** Monitors performance and adapts difficulty.  
**Responsibilities:** Simplify or increase challenge, provide periodic reviews.  
**Tools:** Metrics computation, memory agent.

---

## Memory Agent
**Role:** Maintains context, tracks weak words, stores progress.  
**Responsibilities:** Remember previous interactions, recall preferences and weak vocabulary.  
**Tools:** Conversation buffer, persistent storage.

---

## CSV Loader Agent
**Role:** Loads user-provided CSV files containing vocabulary or exercises.  
**Responsibilities:** Read files, handle errors, structure data, notify planner.  
**Tools:** Pandas, file system access, validation routines.

---

## Data Analysis Agent
**Role:** Analyze user performance and imported data to generate insights.  
**Responsibilities:** Identify patterns, compute statistics, highlight weak areas.  
**Tools:** Pandas, NumPy, visualization libraries, memory integration.

---

## Report Generation Agent
**Role:** Generate user-friendly progress reports.  
**Responsibilities:** Summarize insights, include charts, save or export reports.  
**Tools:** Markdown/PDF/HTML formatters, visualization libraries, file system access.
