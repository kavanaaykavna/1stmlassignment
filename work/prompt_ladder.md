# Prompt Ladder

## Baseline Prompt (Weak Prompt)

### Prompt

> Explain this SEO dataset.

### Representative Output

> This dataset contains SEO metrics such as impressions, clicks, CTR, rankings, and content information. It can be used for machine learning and SEO analysis.

### Notes

**What changed?**

- This is the baseline prompt with no additional guidance.

**What actually improved in the output?**

- Nothing. This serves as the starting point for comparison.

**What still failed?**

- The response is too generic and does not explain how the dataset relates to my machine learning project.

**What would I try next?**

- Add a clear goal so the AI understands exactly what I want.

---

# Version 1 – Add a Clear Goal

### Layer Added

**Clear Goal**

### Prompt

> Explain this SEO dataset so I can understand how it will help me build a machine learning model to identify webpages with declining search performance.

### Representative Output

> The explanation focuses on how the dataset supports prediction instead of only describing the columns.

### Notes

**What changed?**

- Added a clear goal.

**What actually improved in the output?**

- The response became more relevant to my project and explained why the dataset is useful for predicting declining webpages.

**What still failed?**

- It still explains concepts that I already know.

**What would I try next?**

- Define the intended audience.

---

# Version 2 – Add an Audience

### Layer Added

**Audience**

### Prompt

> Explain this SEO dataset for a second-year Computer Science student who already understands basic Python and machine learning concepts.

### Representative Output

> The explanation skips beginner programming topics and focuses on understanding the dataset and its features.

### Notes

**What changed?**

- Added the intended audience.

**What actually improved in the output?**

- The response became more appropriate for my background and stopped explaining basic programming concepts.

**What still failed?**

- It still lacks context about my internship project.

**What would I try next?**

- Add project-specific context.

---

# Version 3 – Add Context

### Layer Added

**Context**

### Prompt

> Explain this SEO dataset for a second-year Computer Science student. I am completing the FlyRank Machine Learning Internship, and my project is to identify webpages that should be prioritized for content refresh.

### Representative Output

> The explanation now connects the dataset directly to the internship project and explains why SEO metrics such as impressions, CTR, average position, and content age are important.

### Notes

**What changed?**

- Added project context.

**What actually improved in the output?**

- The explanation became specific to my internship and related the dataset to the business problem I am solving.

**What still failed?**

- The response is still long and difficult to scan.

**What would I try next?**

- Specify the desired output format.

---

# Version 4 – Specify the Output Format

### Layer Added

**Output Format**

### Prompt

> Explain the dataset using the following sections:
>
> 1. Dataset Purpose
> 2. Unit of Analysis
> 3. Target Variable
> 4. Important Features
> 5. Why These Features Matter
> 6. Summary

### Representative Output

> The explanation is organized into clearly labeled sections, making it easier to understand and reference.

### Notes

**What changed?**

- Added a required output format.

**What actually improved in the output?**

- The information became much easier to read because it was organized into logical sections.

**What still failed?**

- Some sections include unnecessary details.

**What would I try next?**

- Add constraints to make the response more concise.

---

# Version 5 – Add Constraints

### Layer Added

**Constraints**

### Prompt

> Explain the dataset using the specified format. Keep the explanation under 300 words, avoid unnecessary SEO jargon, and include only information useful for building the machine learning model.

### Representative Output

> The explanation is concise, focused, and directly useful for understanding how the dataset supports the machine learning task.

### Notes

**What changed?**

- Added constraints.

**What actually improved in the output?**

- The response became shorter, more focused, and easier to use as a quick reference while working on the project.

**What still failed?**

- Because the response is shorter, it leaves out some background information that could help someone who is completely new to SEO.

**What would I try next?**

- No additional changes are needed. This version balances clarity, relevance, and conciseness well.

---

# Final Reusable Prompt

Explain the SEO dataset for a second-year AIML student completing the FlyRank Machine Learning Internship.

My project is to identify webpages that should be prioritized for content refresh using machine learning.

Use the following structure:

1. Dataset Purpose
2. Unit of Analysis
3. Target Variable
4. Important Features
5. Why These Features Matter
6. Summary

Keep the explanation under 300 words. Avoid unnecessary SEO jargon and include only information that helps build and understand the machine learning model.

---

# Reflection

This exercise showed me that improving a prompt one step at a time produces much better results than changing many things at once. Adding a clear goal made the response more relevant, defining the audience reduced unnecessary explanations, adding project context connected the answer to my internship, specifying an output format improved readability, and adding constraints made the response concise and practical. It also showed that every improvement has trade-offs—for example, making the answer shorter also removes some helpful background information.
