# React Foundations — Notes (Chapters 1–7)

This file collects quick notes and the answers to the "Check Your Understanding" questions for the React Foundations (Next.js) tutorial. Keep this in the repository so you can share progress and review later.

## Chapter checklist
- [ ] 1 — About React and Next.js
- [ ] 2 — Rendering User Interfaces (UI)
- [ ] 3 — Updating UI with JavaScript
- [ ] 4 — Getting Started with React
- [ ] 5 — Building UI with Components
- [ ] 6 — Displaying Data with Props
- [ ] 7 — Adding Interactivity with State

Complete each box as you work through the tutorial and add short notes under each chapter heading (or create a `chapters/` folder if you prefer one file per chapter).

## Quick answers — Check Your Understanding

1) What is the DOM?

- The Document Object Model (DOM) is an in-memory tree representation of an HTML (or XML) document. Each element, attribute and text node is an object that JavaScript can query and change. Browsers expose DOM APIs to let scripts read and modify page structure, content and styles.

2) Imperative vs Declarative

- Imperative: you give explicit step-by-step instructions to reach a result (e.g., select an element, create nodes, append children). It's like following a recipe.
- Declarative: you describe the desired UI state and let the framework handle the steps to produce it (React is declarative — you render components from state). It's like ordering a pizza.

3) What is JSX?

- JSX is a JavaScript syntax extension that looks like HTML/XML. It is compiled into JavaScript calls (e.g., React.createElement or runtime helpers) that produce virtual DOM nodes. JSX is optional but makes component templates clearer.

4) What is Babel?

- Babel is a JavaScript compiler/transpiler that converts modern JS (and JSX) into syntax runnable on current engines. It performs syntax transforms and can inject polyfills. (Note: Babel compiles; it is not a runtime interpreter.)

5) Props vs State

- Props: read-only values passed from a parent to a child component. They make components configurable and reusable.
- State: local, mutable data owned by a component (e.g., via useState). Updating state triggers re-renders for that component and its subtree.

## How to run the scaffold locally

From the repository root:

```powershell
cd C:\Users\nehik\wdd430-react-foundations\my-react-foundation
npm run dev
```

Build for production:

```powershell
npm run build
```

## Chapter folders — do you need them?

- Not required. You can keep notes in this single `NOTES.md` at the repo root or inside the `my-react-foundation` folder. Creating a `chapters/` directory with one file per chapter (for example `chapters/01-about-react.md`) can make review and grading easier and keeps notes organized.
- Recommendation: create a `chapters/` folder if you plan to add code examples, screenshots, or multiple notes per chapter. Otherwise `NOTES.md` is fine.

## Next steps (suggested)
- Finish and check-off chapters 1–7 in this file.
- Add small demo components under `src/components/` that illustrate props and state (e.g., a Counter component with `useState`).
- When ready, push the `feat/react-foundations` branch and open a PR to `main`.

---
Created: 2025-11-05 — initial notes and answers for Chapters 1–7
