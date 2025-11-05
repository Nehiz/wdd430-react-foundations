WDD430 - React Foundations

## Course Information

- Course: WDD430 - Web Frontend Development II
- Institution: Brigham Young University
- Project: From JavaScript to React - React Foundations Tutorial

## Project Overview

This repository contains my work from the Next.js React Foundations tutorial as part of WDD430. The project focuses on learning essential JavaScript concepts and introducing core React concepts through hands-on practice.

## Learning Objectives

- Review essential JavaScript concepts needed for React development
- Understand the Document Object Model (DOM) and UI rendering
- Learn the difference between imperative and declarative programming
- Master React fundamentals including components, props, and state
- Gain experience with JSX syntax
- Build interactive user interfaces with React

## Tutorial Chapters Completed

### Week 1 (Chapters 1-7)

- Chapter 1: About React and Next.js | Completed
- Chapter 2: Rendering User Interfaces (UI)
- Chapter 3: Updating UI with JavaScript
- Chapter 4: Getting Started with React
- Chapter 5: Building UI with Components
- Chapter 6: Displaying Data with Props
- Chapter 7: Adding Interactivity with State

### Week 2 (Remaining Chapters)

To be completed...

## Technologies Used

- JavaScript (ES6+) - Core programming language
- React - JavaScript library for building user interfaces
- Next.js - React framework for production
- HTML/CSS - Markup and styling
- Node.js - Runtime environment
- npm - Package manager

## Getting Started

### Prerequisites

```powershell
node --version  # v18.0.0 or higher
npm --version   # v8.0.0 or higher
```

### Installation

Clone the repository:

```powershell
git clone https://github.com/Nehiz/wdd430-react-foundations.git
cd wdd430-react-foundations
```

Install dependencies (inside the Next.js app folder):

```powershell
cd my-react-foundation
npm install
```

Run the development server:

```powershell
npm run dev
```

Open http://localhost:3000 in your browser.

## Project Structure

```
## Project Structure
```

wdd430-react-foundations/
├── chapters/          # Tutorial chapter exercises
├── src/               # Main application source code
│   └── app/           # Next.js app directory
├── public/            # Static assets
├── node_modules/      # Dependencies (not committed)
├── README.md          # Project documentation
├── NOTES.md           # Personal notes
├── package.json       # Project dependencies
└── next.config.mjs    # Next.js configuration

```
## Key Concepts Learned

### DOM (Document Object Model)

The DOM is a programming interface for web documents that represents the page structure as a tree of objects that can be manipulated with JavaScript.

### Imperative vs Declarative Programming

- Imperative: Step-by-step instructions (how to do something)
- Declarative: Describe what you want (what should be done)

### JSX (JavaScript XML)

A syntax extension for JavaScript that allows writing HTML-like code in JavaScript files. It makes React components easier to read and write.

### Props vs State

- Props: Read-only data passed from parent to child components
- State: Mutable data managed within a component that can change over time

## Resources

- Next.js Learn Tutorial: https://nextjs.org/learn
- Essential JavaScript for React: https://nextjs.org/learn/essentials/javascript-for-react
- React Documentation: https://reactjs.org/docs/getting-started.html
- Next.js Documentation: https://nextjs.org/docs

## Progress Tracking

| Chapter | Title | Status | Completion Date |

| 1 | About React and Next.js | Completed | Nov. 5th, 2025 |
| 2 | Rendering User Interfaces | Pending | - |
| 3 | Updating UI with JavaScript | Pending | - |
| 4 | Getting Started with React | Pending | - |
| 5 | Building UI with Components | Pending | - |
| 6 | Displaying Data with Props | Pending | - |
| 7 | Adding Interactivity with State | Pending | - |



## Reflection

[Add your personal reflections and key takeaways after completing the modules]

## Author

Nehikhare Efehi — BYU WDD430 Student — enehikhare@byui.edu

## License

This project is created for educational purposes as part of BYU coursework.

## Notes on project structure 

- My current setup keeps the Next.js app in `my-react-foundation/` inside the repository. This is a good approach because I plan to store course notes, multiple small projects, or documentation at the repo root.
- If you prefer the Next.js app to be the repository root (simpler for deployment and typical for single-project repos), you can move the app files up to the repo root. If you do that, remove any extra top-level `package-lock.json` (we observed multiple lockfiles earlier) to avoid Next.js workspace warnings.

Commands to move the app to repo root (optional):

```powershell
# from repo root
Move-Item -Path .\\my-react-foundation\\* -Destination . -Force
Remove-Item -Path .\\my-react-foundation -Recurse -Force
```

Or keep the current structure and use the `my-react-foundation` folder as the project root when running scripts.

## Getting Started

First, run the development server:

```bash
npm run dev
# or
yarn dev
# or
pnpm dev
# or
bun dev
```

Open [http://localhost:3000](http://localhost:3000) with your browser to see the result.

You can start editing the page by modifying `app/page.js`. The page auto-updates as you edit the file.

This project uses [`next/font`](https://nextjs.org/docs/app/building-your-application/optimizing/fonts) to automatically optimize and load [Geist](https://vercel.com/font), a new font family for Vercel.

## Learn More

To learn more about Next.js, take a look at the following resources:

- [Next.js Documentation](https://nextjs.org/docs) - learn about Next.js features and API.
- [Learn Next.js](https://nextjs.org/learn) - an interactive Next.js tutorial.

You can check out [the Next.js GitHub repository](https://github.com/vercel/next.js) - your feedback and contributions are welcome!

## Deploy on Vercel

The easiest way to deploy your Next.js app is to use the [Vercel Platform](https://vercel.com/new?utm_medium=default-template&filter=next.js&utm_source=create-next-app&utm_campaign=create-next-app-readme) from the creators of Next.js.

Check out our [Next.js deployment documentation](https://nextjs.org/docs/app/building-your-application/deploying) for more details.
