# Spec Driven Design (SDD) with LLM

A collection of structured prompts for implementing Spec Driven Design methodology using Large Language Models. This repository provides a systematic approach to transform ideas into well-defined requirements, comprehensive designs, and actionable implementation plans.

## Overview

Spec Driven Design is a methodology that breaks down feature development into three distinct phases:

1. **Requirements Gathering** - Transform ideas into detailed, testable requirements
2. **Design Creation** - Develop comprehensive technical designs based on requirements
3. **Task Planning** - Create actionable implementation plans for developers

This approach ensures thorough planning before coding begins, reducing development time and improving code quality.

## Repository Structure

```
kiro-style-sdd/
├── README.md          # This file
├── spec.md           # Phase 1: Requirements gathering prompt
├── design.md         # Phase 2: Design creation prompt  
├── tasks.md          # Phase 3: Task planning prompt
├── implement.md      # Implementation guidance prompt
└── specs/            # Your project specifications (create as needed)
    └── your_project/ # Example project folder structure
        ├── requirements.md
        ├── design.md
        └── tasks.md
```

## Getting Started

### Step 1: Create Your Project Folder

Create a new folder for your project under the `specs/` directory:

```bash
mkdir -p specs/your_project_name
cd specs/your_project_name
```

Replace `your_project_name` with a descriptive name for your feature or application.

### Step 2: Requirements Phase

1. **Start a new conversation** with your preferred LLM (works particularly well with **Gemini 2.5 Pro**)
2. **Copy and paste the entire content** of `spec.md` into the chat
3. **Describe your feature idea** when prompted
4. **Review the generated requirements.md** carefully
5. **Ask for clarifications or modifications** until you're completely satisfied
6. **Save the final requirements.md** in your project folder

**Example interaction:**

```
User: [Paste spec.md content]
User: I want to build a task management app with real-time collaboration

LLM: [Generates initial requirements.md]
User: Can you add requirements for user authentication and file attachments?
LLM: [Updates requirements.md]
User: The requirements look good! We can move on to design.
```

### Step 3: Design Phase

1. **In the same conversation** (to maintain context), copy and paste the content of `design.md`
2. **Review the generated design.md** thoroughly
3. **Request modifications** as needed
4. **Approve the design** only when satisfied
5. **Save the final design.md** in your project folder

**Important:** Use the same chat conversation to maintain context with the requirements.

### Step 4: Task Planning Phase

1. **Continue in the same conversation**, copy and paste the content of `tasks.md`
2. **Review the generated task list**
3. **Refine tasks** until they're actionable and complete
4. **Approve the final task plan**
5. **Save the final tasks.md** in your project folder

### Step 5: Implementation

Once you have all three documents (requirements.md, design.md, tasks.md):

1. **Use any coding assistant** (Claude, ChatGPT, Copilot, etc.)
2. **Copy and paste the content of `implement.md`**
3. **Provide the path to your project folder** containing the three spec documents
4. **Ask the assistant to implement specific tasks** from your tasks.md file

**Example:**

```
User: [Paste implement.md content]
User: Please implement task 2.1 from the tasks in /path/to/specs/my_project/
```

## Best Practices

### ✅ Do's

- **Maintain context** by using the same conversation for requirements → design → tasks
- **Review thoroughly** at each phase before moving to the next
- **Be specific** when requesting changes or clarifications
- **Save documents** after each phase completion
- **Implement one task at a time** during the coding phase

### ❌ Don'ts

- **Don't skip phases** - each builds on the previous one
- **Don't rush approvals** - thorough review saves time later
- **Don't start new conversations** between phases (loses context)
- **Don't implement multiple tasks simultaneously**
- **Don't modify documents manually** - use the LLM for consistency

## Example Workflow

Here's a complete example of the SDD process:

### 1. Requirements Phase

```markdown
📁 specs/todo_app/
└── requirements.md ✅ (Created and approved)
```

### 2. Design Phase  

```markdown
📁 specs/todo_app/
├── requirements.md ✅
└── design.md ✅ (Created and approved)
```

### 3. Task Planning Phase

```markdown
📁 specs/todo_app/
├── requirements.md ✅
├── design.md ✅
└── tasks.md ✅ (Created and approved)
```

### 4. Implementation Phase

```markdown
📁 specs/todo_app/
├── requirements.md ✅
├── design.md ✅
├── tasks.md ✅
└── src/ (Implementation begins)
    ├── models/
    ├── services/
    └── tests/
```

## Why This Works

### Systematic Approach

- **Structured thinking** prevents overlooking important aspects
- **Iterative refinement** ensures quality at each phase
- **Context preservation** maintains consistency across phases

### LLM Optimization

- **Specific prompts** guide the LLM to produce consistent, high-quality outputs
- **Phase separation** prevents overwhelming the model with too much context
- **Approval gates** ensure human oversight at critical decision points

### Development Benefits

- **Reduced rework** through thorough upfront planning
- **Clear implementation path** with actionable tasks
- **Better estimates** from detailed task breakdown
- **Improved code quality** through test-driven approach

## Recommended LLMs

While this methodology works with most modern LLMs, we recommend:

1. **Gemini 2.5 Pro** - Excellent for the full SDD workflow
2. **Claude 3.5 Sonnet** - Great for requirements and design phases
3. **ChatGPT-4** - Good all-around performance
4. **Any coding-focused LLM** for the implementation phase

## Troubleshooting

### Common Issues

**Q: The LLM isn't following the prompt structure**

- Ensure you're copying the entire prompt content
- Try rephrasing your feature description
- Use a different LLM model

**Q: Requirements seem incomplete**

- Ask specific questions about edge cases
- Request additional user stories
- Ask for clarification on technical constraints

**Q: Design doesn't match requirements**

- Point out specific mismatches
- Ask the LLM to review requirements again
- Request design revisions for specific sections

**Q: Tasks are too vague or too detailed**

- Ask for more specific implementation steps
- Request task breakdown or consolidation
- Clarify the scope of individual tasks

## Contributing

This repository is a collection of prompts. To contribute:

1. Test prompts with multiple LLMs
2. Suggest improvements to prompt clarity
3. Share successful project examples
4. Report issues with specific LLM models

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## Support

For questions or issues:

1. Check the troubleshooting section above
2. Review your prompt usage against the examples
3. Try with a different LLM model
4. Open an issue in this repository

---

**Happy Spec Driven Development! 🚀**
