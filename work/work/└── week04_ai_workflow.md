# Week 4 – AI Workflow (Build Core)

## Workflow Name

**AI Writing Assistant Workflow for Technical Assignments**

---

# Why I Chose This Workflow

During my internship, I frequently write technical assignments, case studies, documentation, and project reports. Instead of writing everything manually, I wanted a workflow that helps me create high-quality drafts, improve them, and prepare them for submission while still keeping final control over the content.

---

# Workflow Diagram

```text
Assignment Topic
      │
      ▼
Step 1 – Draft
Generate the first draft using AI
      │
      ▼
Step 2 – Critique
Review the draft for clarity, grammar,
missing information, and structure
      │
      ▼
Step 3 – Revise
Generate the improved final version
      │
      ▼
Human Review
Verify technical accuracy and submit
```

---

# Workflow Tools

- Claude Project
- ChatGPT
- Markdown (.md)

No backend or coding workflow is required.

---

# Step 1 – Draft

## Purpose

Generate the initial version of the assignment.

### Prompt

```text
Write a clear technical assignment using simple English.
Use proper headings, concise explanations, and maintain a professional tone.
```

### Input

Assignment topic

### Output

First draft

---

# Step 2 – Critique

## Purpose

Review the draft and identify improvements.

### Prompt

```text
Review the draft as an experienced mentor.

Identify:
- Grammar mistakes
- Missing information
- Unclear explanations
- Repetition
- Formatting improvements

Provide suggestions only.
```

### Input

Draft from Step 1

### Output

List of improvements

---

# Step 3 – Revise

## Purpose

Create the final polished assignment.

### Prompt

```text
Improve the assignment using the review feedback.

Keep the technical meaning unchanged while improving readability,
grammar, structure, and formatting.

Return the final version ready for submission.
```

### Input

Draft + critique

### Output

Final submission-ready assignment

---

# Five Real Workflow Runs

| Run | Input | Result |
|------|-------|--------|
| 1 | Identity Kit | Generated, reviewed, and finalized the portfolio identity kit. |
| 2 | Content Map | Improved page organization and call-to-actions. |
| 3 | Three Roads Assignment | Compared three technology stacks and selected React + Vite. |
| 4 | Week 3 Data Contract | Improved documentation and clarified feature descriptions. |
| 5 | Portfolio Homepage Content | Generated and refined homepage introduction for the portfolio. |

---

# Time Comparison

## Manual Process

Average time per assignment:

**30 minutes**

Five assignments:

**150 minutes**

---

## AI Workflow

Average time per assignment:

**10 minutes**

Five assignments:

**50 minutes**

---

## Estimated Time Saved

Approximately **100 minutes (around 67%)**, excluding the initial workflow setup.

---

# Known Failure Points

Although the workflow saves time, it still has limitations.

- AI may misunderstand vague prompts.
- AI may repeat information.
- AI may generate incorrect technical details.
- AI may not perfectly match assignment requirements.
- AI cannot verify factual accuracy automatically.

---

# Human Review Required

Human review is still necessary to:

- Verify technical correctness.
- Confirm project-specific details.
- Check repository links.
- Ensure screenshots and evidence are correct.
- Confirm the assignment follows the required format.

---

# What I Learned

Breaking the writing process into separate steps produces better results than asking AI to generate everything in a single prompt. Reviewing and revising the draft significantly improves clarity, structure, and overall quality while reducing the total time spent on documentation.

---

# Conclusion

I built a three-step AI writing workflow consisting of Draft → Critique → Revise. The workflow successfully handled five real assignments from my internship, reduced writing time, and improved consistency. While AI accelerates documentation, human review remains essential for verifying technical accuracy and ensuring the final submission meets all assignment requirements.
