```markdown
# Chapter 3 — Updating UI with JavaScript

Summary

- I learned that in plain JavaScript I update the DOM imperatively, but in React I describe the desired UI state and let the framework handle DOM updates declaratively.

What I need to remember

- Prefer declarative updates with state/hooks over manual DOM operations.
- Understand how events, controlled inputs, and state lifecycles affect re-renders.

# Chapter 3 — Updating UI with JavaScript

Summary

- I learned the difference between imperative DOM manipulation (manual steps) and React's declarative approach (describe the UI for a given state and let React update the DOM).

Imperative (plain JavaScript) example

```html
<!-- index.html (vanilla JS) -->
<div id="counter">0</div>
<button id="inc">+1</button>

<script>
	const el = document.getElementById('counter');
	## Chapter 3 — Updating UI with JavaScript

	In this chapter I practice updating the UI directly with JavaScript and DOM methods, then compare that imperative approach with React's declarative model.

	Getting started — minimal HTML example

	Create `index.html` with a target div and a script tag:

	```html
	<!doctype html>
	<html>
		<body>
			<div id="app"></div>
			<script type="text/javascript">
				// Select the div element with 'app' id
				const app = document.getElementById('app');

				// Create a new H1 element
				const header = document.createElement('h1');

				// Create a new text node for the H1 element
				const text = 'Develop. Preview. Ship.';
				const headerContent = document.createTextNode(text);

				// Append the text to the H1 element
				header.appendChild(headerContent);

				// Place the H1 element inside the div
				app.appendChild(header);
			</script>
		</body>
	</html>
	```

	When I open this file in the browser I see the H1 text. The DOM (viewed in devtools) now contains the `<h1>` even though the original source HTML didn't.

Understanding What Just Happened
The Code Breakdown:
// 1. SELECT the target element
const app = document.getElementById('app');

// 2. CREATE a new element
const header = document.createElement('h1');

// 3. CREATE text content
const headerContent = document.createTextNode('Develop. Preview. Ship.');

// 4. PUT text inside the h1
header.appendChild(headerContent);

// 5. PUT the h1 inside the div
app.appendChild(header);

This is 5 steps just to add one heading! This is imperative programming - you're telling the computer HOW to do it step-by-step.

	Imperative vs Declarative programming

	- Imperative: I write step-by-step instructions for how to change the UI (create elements, append children, update text). The example above is imperative.
	- Declarative: I describe the desired UI for a given state (for example, "render an H1 with this text") and the framework figures out how to update the DOM. React is declarative.

	Why declarative is helpful for UIs

	- Less boilerplate: I don't manage DOM nodes and manual updates.
	- Easier to reason about: components describe "what" to render based on state/props.
	- Fewer bugs and better performance: React batches updates and reconciles changes efficiently.
	- Controlled inputs make form state explicit and easier to validate; uncontrolled inputs (using refs) are fine for simple scenarios.

	Reconciliation and performance

	- React keeps a virtual representation of the UI and compares it to the previous version to apply only necessary changes to the DOM (reconciliation).
	- For performance-sensitive areas I can:
		- memoize components with `React.memo`
		- avoid passing new object/array props unless necessary
		- split large components into smaller pieces to reduce re-renders


	Check Your Understanding

	- What steps did I write imperatively to add an `<h1>` to the page?

		- I selected the target element (document.getElementById), created a new element (document.createElement), created and attached text (createTextNode + appendChild), and inserted the element into the DOM (appendChild).

	- How does the DOM differ from the original HTML after JavaScript runs?

		- HTML is the initial source code I write. The DOM is the live, updated representation that JavaScript can modify — it shows the current page structure after scripts run.

	- What advantages does a declarative UI library like React provide over manual DOM manipulation?

		- React lets me describe WHAT the UI should be for a given state and it figures out HOW to update the DOM. This reduces boilerplate, makes code easier to reason about, and helps avoid manual DOM bugs. React also optimizes updates via reconciliation.

	Checklist

	- [ ] Try the `chapters/chapter-03/index.html` example and confirm the `<h1>` appears
	- [ ] Run the Next.js dev server and visit `/dom-example` to compare declarative vs imperative
	- [ ] Explain in my own words the difference between imperative and declarative approaches
	- [ ] Read the next chapter on getting started with React
