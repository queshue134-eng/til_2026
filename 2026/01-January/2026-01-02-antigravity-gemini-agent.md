# 2026-01-02 TIL: How to Use AntiGravity (Gemini AI Coding Agent) Effectively

## Category: AI Tools / Developer Productivity

### Video Reference

[![YouTube](https://img.shields.io/badge/YouTube-Video-red?style=flat-square&logo=youtube)](https://www.youtube.com/watch?v=QZCYFJTv8jI)

### Key Takeaways

**AntiGravity** is Google DeepMind's agentic AI coding assistant built on Gemini. It's designed to pair program with developers, autonomously executing complex coding tasks while maintaining context awareness.

---

## 🚀 What is AntiGravity?

AntiGravity is an **agentic coding assistant** that differs from traditional AI chat:

| Feature      | Traditional AI Chat | AntiGravity            |
| ------------ | ------------------- | ---------------------- |
| Execution    | Suggests code       | Actually runs commands |
| File access  | None                | Full read/write access |
| Context      | Single conversation | Workspace-aware        |
| Autonomy     | Reactive            | Proactive              |
| Verification | Manual              | Automated testing      |

---

## 💡 Best Practices for Using AntiGravity

### 1. Be Specific with Context

Instead of vague requests, provide:

- The specific file or function you're working on
- Expected behavior vs actual behavior
- Any constraints or preferences

**❌ Bad:** "Fix the bug"
**✅ Good:** "The `calculateTotal()` function in `cart.js` returns NaN when the cart is empty. It should return 0."

### 2. Leverage Its Agentic Nature

AntiGravity can:

- Create entire project structures
- Run and verify tests
- Search the codebase for patterns
- Update multiple files consistently
- Commit changes to Git

### 3. Use Workflows

Create `.agent/workflows/*.md` files to define repeatable processes:

- Deployment procedures
- Testing protocols
- Code review checklists

### 4. Let It Verify Its Work

AntiGravity can run commands to verify changes:

- Execute test suites
- Build the project
- Run linters
- Start dev servers

### 5. Provide Feedback

When AntiGravity makes mistakes:

- Explain what went wrong
- It learns from corrections within the session
- Use "undo" language for quick reversals

---

## 🛠️ Common Use Cases

| Task              | Example Prompt                                        |
| ----------------- | ----------------------------------------------------- |
| **New Feature**   | "Add a dark mode toggle to the settings page"         |
| **Bug Fix**       | "Users report login fails on Safari. Debug and fix."  |
| **Refactoring**   | "Extract the API calls into a separate service layer" |
| **Documentation** | "Generate JSDoc comments for all public functions"    |
| **Testing**       | "Write unit tests for the authentication module"      |
| **DevOps**        | "Create a GitHub Actions workflow for CI/CD"          |

---

## ⚡ Power User Tips

### Use Artifacts Effectively

AntiGravity creates artifacts like:

- `task.md` — Tracks progress on complex tasks
- `implementation_plan.md` — Documents planned changes
- `walkthrough.md` — Summarizes completed work

### Batch Related Changes

Instead of making many small requests, batch related changes:

> "Refactor the user module: rename `getUser` to `fetchUser`, add TypeScript types, and update all call sites."

### Trust the Process

For complex tasks, AntiGravity will:

1. **Plan** — Analyze and create an implementation plan
2. **Execute** — Make changes systematically
3. **Verify** — Run tests and validate changes

### Use Browser Capabilities

AntiGravity can:

- Navigate web pages
- Take screenshots
- Test web applications
- Record browser sessions

---

## 🔒 Safety Features

| Feature              | Description                                |
| -------------------- | ------------------------------------------ |
| **Command approval** | Destructive commands require user approval |
| **SafeToAutoRun**    | Only safe commands run automatically       |
| **Workspace limits** | Cannot access files outside workspace      |
| **Git safety**       | Always pulls before pushing                |

---

## 🎯 When to Use AntiGravity vs Other Tools

| Scenario                   | Best Tool           |
| -------------------------- | ------------------- |
| Quick code questions       | Regular Gemini chat |
| Complex multi-file changes | **AntiGravity**     |
| Learning concepts          | Regular Gemini chat |
| Building features          | **AntiGravity**     |
| Debugging with context     | **AntiGravity**     |
| One-liner scripts          | Either              |

---

### Additional Resources

- [Gemini AI](https://gemini.google.com/)
- [Google DeepMind](https://deepmind.google/)
- [Original Video: How to Use AntiGravity Better than 99% of People](https://www.youtube.com/watch?v=QZCYFJTv8jI)
