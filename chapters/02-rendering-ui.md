# Chapter 2 — Rendering User Interfaces (UI)

Summary

- I learned that the DOM (Document Object Model) is an object representation of HTML elements and acts as a bridge between my code and the user interface. It has a tree-like structure with parent/child relationships.

- I learned how browsers render pages: Server → HTML file → Browser → DOM → User interface.

Key Concepts

1. The DOM (Document Object Model)

- What it is: An object representation of HTML elements.
- Purpose: Acts as a bridge between my code and the user interface.
- Structure: A tree-like structure with parent and child relationships.

2. How Browsers Render Pages

- Flow: Server → HTML file → Browser → DOM → User Interface.

3. DOM Manipulation

With JavaScript and DOM methods I can:

- ✅ Listen to user events (clicks, typing, etc.)
- ✅ Select specific elements
- ✅ Add new elements
- ✅ Update existing elements
- ✅ Delete elements
- ✅ Change styles and content

Visual Analogy

Think of the DOM like a family tree:

<html> (grandparent)
  └── <body> (parent)
	  ├── <header> (child)
	  │    └── <h1> (grandchild)
	  └── <main> (child)
		  └── <p> (grandchild)

Check Your Understanding

Before moving to Chapter 3, I should be able to answer:

- What is the DOM?
- Why is the DOM important for web development?
- What kinds of things can I do with DOM manipulation?

Checklist

- [ ] Read chapter text
- [ ] Add notes or examples here

# Chapter 2 — Rendering User Interfaces (UI)

Summary

- The DOM is the browser's in-memory representation of HTML. React uses a virtual representation and reconciles changes to update the DOM efficiently.
- Rendering can be static (SSG), server-side (SSR), or client-side depending on your needs.

Key takeaways

- Minimize direct DOM manipulation in React; instead, update component state/props.
- Next.js provides multiple rendering modes depending on the page and data needs.

Checklist

- [ ] Read chapter text
- [ ] Add notes or examples here
