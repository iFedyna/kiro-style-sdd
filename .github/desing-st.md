
### 2. Create Learning Design Document

Now you will develop a comprehensive **Learning Design Document** based on the approved learning requirements. This involves researching effective teaching methods for the topic and structuring the lesson plan.

The design document must be based on the `requirements.md` file, so ensure it exists first.

**Constraints:**
* The model MUST create a '.kiro/specs/{feature_name}/design.md' file if it doesn't already exist
*   The model MUST identify areas where pedagogical research is needed (e.g., "What are common misconceptions when learning Python functions?", "What are the best analogies for explaining classes?").
*   The model MUST conduct this research to inform the lesson's structure and content.
*   The model SHOULD NOT create separate research files but use the research as context for the design.
*   The model MUST summarize key findings that will inform the learning design (e.g., "Research indicates learners often confuse parameters and arguments, so the design will address this explicitly with a clear analogy.").
*   The model SHOULD cite sources (e.g., high-quality tutorials, documentation) that inform the teaching strategy.
*   The model MUST incorporate research findings directly into the design.
*   The model MUST create a `design.md` file in the same spec folder and include the following sections:
    *   **Lesson Overview:** A brief summary of the lesson's goal and teaching approach.
    *   **Module Flow & Structure:** The sequence of topics. How the lesson will progress from one concept to the next.
    *   **Learning Components:** A breakdown of the types of content to be used (e.g., theoretical explanations, interactive code examples, visual aids, practical exercises).
    *   **Core Code Examples:** Descriptions of the primary code examples that will be used to demonstrate key concepts.
    *   **Addressing Common Misconceptions:** A plan for proactively identifying and clarifying points that typically confuse learners.
    *   **Assessment Strategy:** How the learner's understanding will be tested (e.g., quizzes, coding challenges, final project description).
    *   **Learning Environment & Tooling:** A description of the setup required for the learner (e.g., "Python 3.9+, VS Code with Python extension").
*   The model SHOULD include diagrams using Mermaid where appropriate to visualize concepts (e.g., a flowchart for a function's logic).
*   The model MUST ensure the design addresses all learning requirements from the previous phase.
*   The model SHOULD highlight key pedagogical decisions and their rationales (e.g., "We will introduce decorators after covering basic functions to avoid cognitive overload.").
*   The model MAY ask the user for input on specific teaching decisions (e.g., "Should we use a simple command-line example or a small web-based one?").
*   After creating or updating the design document, the model MUST ask the user: **"Does this learning design look effective? If so, we can move on to creating the task list."**
*   The model MUST make modifications to the design document if the user requests changes.
*   The model MUST ask for explicit approval after every iteration of edits.
*   The model MUST NOT proceed to the task list phase until receiving clear approval.
*   The model MUST continue the feedback-revision cycle until explicit approval is received.
*   The model MUST offer to return to the requirements gathering phase if gaps in the learning objectives are identified during the design process.

</workflow-definition> to be continued...