# React Foundations — Notes (Chapters 1–7)

This file collects quick notes and the answers to the "Check Your Understanding" questions for the React Foundations (Next.js) tutorial.

## Chapter checklist

- [ ] 1 — About React and Next.js
- [ ] 2 — Rendering User Interfaces (UI)
- [x] 3 — Updating UI with JavaScript
- [x] 4 — Getting Started with React
- [x] 5 — Building UI with Components
- [x] 6 — Displaying Data with Props
- [ ] 7 — Adding Interactivity with State

## Chapter 1 Summary - Key Takeaways

Here's what I've learned:

Main Concepts:

- React = JavaScript library for building interactive UIs

 	- Provides helpful functions/APIs
 	- Relatively unopinionated about application architecture
 	- Focuses primarily on the UI layer

- Next.js = React framework that adds structure and features

 	- Handles tooling and configuration
 	- Provides solutions for routing, data fetching, caching
 	- Optimizes both developer and user experience

Building Blocks of Web Applications:

- User Interface
- Routing
- Data Fetching
- Rendering
- Integrations
- Infrastructure
- Performance
- Scalability
- Developer Experience

Key Distinction:

- Library (React): Gives you tools but you decide how to use them
- Framework (Next.js): Provides structure, conventions, and additional features on top of React

## Quick answers to the "Check Your Understanding" questions

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

Created: 2025-11-05 — initial notes and answers for Chapters 1–7
Updated: 2025-11-10 — Chapters 3, 4, 5, and 6 marked complete; Chapter 5 demo added at `chapters/chapter-05/index.html` and Chapter 6 demo at `chapters/chapter-06/index.html`.

## Deployment

Two easy options for deploying this repository's Next.js app which lives in `my-react-foundation/`:

- Vercel (recommended for Next.js)
 	- When creating the project in Vercel, set the "Root Directory" to `my-react-foundation` so Vercel runs install/build from that folder.
 	- If you use the Vercel CLI or GitHub integration, provide a Vercel token and set the project/organization in the dashboard.

- GitHub Actions (CI) — build artifact example
 	- Add a workflow that builds the Next app from the `my-react-foundation/` directory. Below is a simple example that runs on push and uploads the `.next` build output as an artifact (you can replace the upload step with a deploy action for your provider):

```yaml
name: Build Next.js (subdirectory)
on:
 push:
  branches: [ main, feat/react-foundations ]
 pull_request:
  branches: [ main ]

jobs:
 build:
  runs-on: ubuntu-latest
  steps:
   - uses: actions/checkout@v4

   - name: Use Node.js 18
    uses: actions/setup-node@v4
    with:
     node-version: '18'

   - name: Install dependencies
    working-directory: my-react-foundation
    run: npm ci

   - name: Build
    working-directory: my-react-foundation
    run: npm run build

   - name: Upload build artifact
    uses: actions/upload-artifact@v4
    with:
     name: next-build
     path: my-react-foundation/.next
```

 - To deploy to Vercel from GitHub Actions, use the official Vercel action and set `VERCEL_TOKEN` as a repository secret. Alternatively, configure Vercel through its GitHub integration and set the project root in the Vercel dashboard.
