# FL-05: Workflow vs Agent and Model Context Protocol (MCP)

## Introduction

Artificial Intelligence systems are becoming more capable by connecting to external tools and data sources. However, terms like *workflow* and *agent* are often used interchangeably even though they represent different concepts. During this assignment, I learned the difference between workflows and agents, explored the Model Context Protocol (MCP), and connected Claude Desktop to GitHub using an MCP server.

---

## Workflow vs Agent

A workflow is a predefined sequence of steps designed to complete a task. Every step is planned beforehand, and the system follows the same process each time. The user decides the order of operations and controls the execution.

An agent, on the other hand, is capable of making decisions while working toward a goal. Instead of following fixed instructions, an agent can decide which tool to use, determine the next action, recover from failures, and continue until the task is complete.

In simple terms:

- A workflow follows instructions.
- An agent makes decisions.

---

## My FL-04 Pipeline

For FL-04, I built a research and writing pipeline consisting of the following stages:

1. Gather information.
2. Summarize the sources.
3. Generate the first draft.
4. Review the draft.
5. Format the final document.

Although AI assisted at every stage, the pipeline remained a workflow because I manually triggered each step. The AI never decided what to do next by itself.

Therefore, my FL-04 project is a **workflow**, not an agent.

---

## What is MCP?

Model Context Protocol (MCP) is an open protocol that allows AI models to communicate with external tools and services in a standard way.

Instead of only responding from the conversation, the AI can access live resources such as GitHub repositories, local files, databases, APIs, and cloud services.

MCP acts like a universal connector between AI and external systems.

---

## The Three MCP Primitives

### 1. Tools

Tools allow the AI to perform actions.

Examples include:

- Reading GitHub repositories
- Creating issues
- Running terminal commands
- Accessing APIs

---

### 2. Resources

Resources provide data that the AI can read.

Examples include:

- Local files
- GitHub repositories
- Documentation
- Databases

---

### 3. Prompts

Prompts are reusable instructions that define how the AI should perform a task.

They help standardize workflows and ensure consistent behavior.

---

## My MCP Setup

I installed Claude Desktop Developer Mode and configured a local GitHub MCP server using Docker.

After connecting my GitHub Personal Access Token, Claude successfully interacted with my GitHub account.

I tested the setup with three tasks:

### Task 1

Listed all repositories in my GitHub account.

### Task 2

Opened my `kavana-portfolio` repository and summarized its structure.

### Task 3

Read the `package.json` file and explained the framework, build tool, dependencies, and scripts.

These tasks required live access to GitHub and could not have been completed through normal chat alone.

---

## How My Workflow Could Become an Agent

My current pipeline requires me to manually start every stage.

To become an agent, it would need additional capabilities such as:

- Automatically deciding when research is sufficient.
- Searching for additional sources if information is incomplete.
- Revising drafts without manual intervention.
- Selecting the appropriate tools automatically.
- Detecting errors and recovering from them.
- Publishing the final result after validation.

The agent would operate toward a goal instead of following fixed instructions.

---

## Conclusion

This assignment helped me understand that workflows and agents are fundamentally different.

A workflow follows predefined steps, while an agent makes decisions independently to achieve a goal.

I also learned how MCP enables AI systems to securely connect with external tools. By setting up a GitHub MCP server in Claude Desktop, I experienced how AI can interact with live repositories rather than relying only on conversation history.

Overall, this exercise improved my understanding of modern AI systems and demonstrated how workflows, agents, and MCP work together to build more capable AI applications.
