Language Learning Partner

## Planner Agent

**Role**

* Orchestrates the conversation and coordinates all specialized agents to fulfill the user’s request.
* Powered by an **LLM**, it decides which agent should act at each step.

**Responsibilities**

* Ask the user for clarification if the request is ambiguous.
* Present the conversation plan to the user (optional).
* Decide the sequence of agent actions: Conversation → Grammar → Vocabulary → Difficulty → Memory → CSV/Data Analysis → Report Generation.
* Monitor the interaction and handle errors.
* Provide final response to the user after all agents act.

**Tools**

* LLM for planning and decision-making.
* Access to other agents as callable tools.
* Conversation memory for context.

---

## Conversation Agent

**Role**

* Handles natural dialogue with the user, keeping the conversation flowing and engaging.

**Responsibilities**

* Greet the user and confirm the language to practice.
* Present prompts, questions, and exercises according to the learning plan.
* Adjust tone and style for a friendly, encouraging experience.

**Tools**

* LLM for chat responses.
* Prompt templates for different difficulty levels.
* Memory buffer for context retention.

---

## Grammar Correction Agent

**Role**

* Detects and corrects grammar, spelling, and sentence structure mistakes.

**Responsibilities**

* Identify errors in user input.
* Provide polite corrections and brief explanations.
* Offer hints instead of full answers when necessary.
* Track recurring mistakes for later review.

**Tools**

* Grammar rules or language APIs.
* LLM for nuanced correction suggestions.
* Memory agent to store frequent mistakes.

---

## Vocabulary Agent

**Role**

* Introduces and explains new words, phrases, and expressions.

**Responsibilities**

* Respond to user queries about word meanings.
* Provide example sentences and pronunciation tips.
* Add difficult words to the user’s learning list for future review.

**Tools**

* Dictionary/translation APIs.
* LLM for example sentences.
* Memory agent to store weak vocabulary.

---

## Difficulty / Progress Agent

**Role**

* Monitors the user’s performance and adapts the learning challenge dynamically.

**Responsibilities**

* Track correct and incorrect responses over time.
* Simplify prompts if the user struggles.
* Increase complexity when the user demonstrates proficiency.
* Provide periodic reviews to reinforce learning.

**Tools**

* Metrics computation (error rate, response speed, fluency).
* Memory agent for performance tracking.

---

## Memory Agent

**Role**

* Maintains context, stores weak words, and tracks the user’s learning progress.

**Responsibilities**

* Remember previous interactions and mistakes.
* Recall user preferences, weak vocabulary, and progress trends.
* Provide context to other agents to inform corrections, vocabulary suggestions, and difficulty adjustments.

**Tools**

* Conversation buffer or persistent storage.
* Optional vector database for advanced memory management.

---

## CSV Loader Agent

**Role**

* Safely loads user-provided CSV files containing vocabulary, exercises, or practice data.

**Responsibilities**

* Read CSV files from local storage or cloud sources.
* Handle errors like missing files or malformed data.
* Convert CSV content into structured data usable by other agents.
* Notify the Planner agent once the data is successfully loaded.

**Tools**

* Pandas for CSV ingestion and data manipulation.
* File system access for fetching files.
* Validation routines for format checking.

---

## Data Analysis Agent

**Role**

* Analyze user data, imported vocabulary lists, or performance logs to generate actionable insights.

**Responsibilities**

* Process structured data from the CSV Loader or session logs.
* Identify patterns in user mistakes and strengths.
* Compute statistics: word mastery, error frequency, progress over time.
* Provide summarized insights to the Planner, Vocabulary, or Difficulty Agents.
* Highlight weak areas for review.

**Tools**

* Pandas / NumPy for data manipulation and analysis.
* Visualization libraries (Matplotlib, Seaborn) for charts.
* Integration with Memory Agent for storing trends.

---

## Report Generation Agent

**Role**

* Create comprehensive, human-readable reports summarizing the user’s language learning progress.

**Responsibilities**

* Take insights from the Data Analysis Agent.
* Generate reports including progress, mistakes, mastered vocabulary, and suggested exercises.
* Format reports in Markdown, PDF, or HTML.
* Provide visualizations such as charts or graphs.
* Save reports for the user and optionally feed insights back to the Planner.

**Tools**

* Markdown/PDF/HTML formatters.
* Visualization libraries (Matplotlib, Seaborn, Plotly).
* File system access for saving and sharing reports.

---

If you want, I can now **update the workflow diagram** to include **all of these agents**, showing their interactions in a complete end-to-end flow for your GitHub repo. Do you want me to do that?
