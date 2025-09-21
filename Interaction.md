
---

## 📄 Interaction.md
```markdown
# Interaction Guide

This document shows sample dialogues and the workflow for the **Language Learning Partner**.

---

## Happy Path: Basic Practice

**User:** "I want to practice German today."  
**AI:** "Hallo! Wunderbar, lass uns anfangen. How do you say 'Good morning' in German?"  
**User:** "Guten Morgen"  
**AI:** "Perfect! That was correct. 😊 Want to try a longer sentence?"

---

## Grammar Mistake Example

**User:** "i going to school everyday"  
**AI:** "✍️ Correction: 'I go to school every day.' Remember: 'I' should always be uppercase; 'every day' is two words."

---

## Vocabulary Request

**User:** "What does 'Schmetterling' mean?"  
**AI:** "'Schmetterling' means butterfly in German. Example: 'Der Schmetterling fliegt im Garten.' Can you try using it in a sentence?"

---

## Pronunciation / Accent Feedback

**User:** "How do I pronounce 'r' in French?"  
**AI:** "The French 'r' is guttural. Try making a sound at the back of your throat. Repeat: 'rue, rouge, rire' slowly and listen to native speakers."

---

## Difficulty Adjustment

- Simplify prompts if the user struggles repeatedly.  
- Increase complexity when the user demonstrates proficiency.  
- Example output: "Great job! Let's try a longer sentence with past tense now."

---

## Review Weak Words

**User:** "I want to review the words I got wrong last time."  
**AI:** "Sure! You often struggle with 'verschieden', 'über', 'wegen'. Let's make 3 example sentences using them now."

---

## Workflow Overview  

```mermaid
flowchart LR
    User([User starts conversation / asks question]) --> Planner[Planner Agent]
    Planner --> Conversation[Conversation Agent]
    Conversation --> Planner
    Planner --> Grammar[Grammar Correction Agent]
    Grammar --> Planner
    Planner --> Vocabulary[Vocabulary Agent]
    Vocabulary --> Planner
    Planner --> Difficulty[Difficulty / Progress Agent]
    Difficulty --> Planner
    Planner --> Memory[Memory Agent]
    Memory --> Planner
    Planner --> CSVLoader[CSV Loader Agent]
    CSVLoader --> DataAnalysis[Data Analysis Agent]
    DataAnalysis --> Planner
    Planner --> ReportGen[Report Generation Agent]
    ReportGen --> Planner
    Planner --> Output["Final Feedback / Report to User"]
