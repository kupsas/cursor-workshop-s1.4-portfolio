# Workshop: Build your personal portfolio with Cursor

Welcome. This repository is **starter code** for a hands-on workshop where you learn **Cursor** (an AI-assisted code editor) by building a real project: a **simple, single-page portfolio website** you can share with others.

You do **not** need to be an expert programmer. Follow the steps in order. If something fails, ask your facilitator or use Cursor’s chat and paste the error message.

---

## What you are building

By the end of the workshop (and optional homework), you will have:

- A **one-page portfolio** with your name, what you do, a few highlights, and a way for people to contact you.
- A project that can be **deployed** to the web (for example on [Vercel](https://vercel.com)) so you get a **live link**.

---

## Tech stack (already chosen for you)

| Piece        | What it is |
| ------------ | ---------- |
| **Next.js**  | A popular way to build websites with React. This repo uses the **App Router** (folders under `src/app`). |
| **TypeScript** | JavaScript with types — helps catch mistakes; Cursor handles a lot of the syntax for you. |
| **Tailwind CSS** | Styling with small utility classes in your HTML/JSX (e.g. `flex`, `text-lg`). |
| **Cursor**   | Where you edit code and **ask the AI** to help write, explain, and fix things. |

---

## Before you start — install these

1. **Node.js** (LTS version) — [https://nodejs.org](https://nodejs.org)  
   - Lets you run `npm` commands and a local web server.

2. **Git** — so you can clone this repo (your instructor may give you a different method).

3. **Cursor** — [https://cursor.com](https://cursor.com)  
   - Open **this folder** as a project: *File → Open Folder* and choose the folder you cloned.

**Check Node:** open a terminal (in Cursor: *Terminal → New Terminal*) and run:

```bash
node -v
npm -v
```

You should see version numbers, not an error.

---

## Right after you clone — do this first

Work through these in order. Stop when you see “Hello World” in the browser.

### Step 1: Go to the project folder

In your terminal:

```bash
cd path/to/S1_PersonalPortfolio
```

(Use the real path where your clone lives.)

### Step 2: Install dependencies

```bash
npm install
```

This downloads the libraries the project needs. It can take a minute the first time.

### Step 3: Start the dev server

```bash
npm run dev
```

### Step 4: Open the site

In your browser, go to: [http://localhost:3000](http://localhost:3000)

You should see a **Hello World** placeholder. That means the boilerplate works.

### Step 5: Keep the terminal running

Leave `npm run dev` running while you work. When you save a file, the page usually **refreshes automatically**.

To stop the server later: focus the terminal and press `Ctrl+C`.

---

## How Cursor fits into this workshop

Cursor is your **pair programmer**. Typical flow:

1. **Open the file** you care about (for example `src/app/page.tsx`).
2. **Chat** (AI panel) or **Composer** (multi-file edits): describe what you want in **plain English**.
3. **Review** the suggested changes before accepting — it is okay to ask “explain this line” or “make it simpler.”

**Tip:** Be specific. Instead of “make it pretty,” try: “Add a Hero section with my name, a one-line tagline, and a button that scrolls to Contact.”

---

## What you will add on the page (four sections)

Build **one section at a time**, test in the browser, then move on. Suggested order:

1. **Hero** — Your name, a short tagline, and a call-to-action (button or link).
2. **About** — A few sentences about you and what you do.
3. **Work / Projects** — About **three or four cards** (projects, designs, or achievements).
4. **Contact** — Email link, social links, and/or a simple form.

Put reusable pieces in **`src/components/`** (e.g. `Hero.tsx`, `About.tsx`) and compose them from **`src/app/page.tsx`**. That keeps your code organized and is how real projects are structured.

---

## Suggested first message to Cursor (after Hello World works)

Decide your **name** and **tagline** (you can write them on paper first). Then try something like:

> “Add a Hero section to my portfolio. My name is [YOUR NAME]. My tagline is [YOUR TAGLINE]. Add a primary button that says [BUTTON LABEL]. Use Tailwind for styling and make it look good on mobile and desktop. Put the Hero in a component under `src/components/` and use it from `src/app/page.tsx`.”

After the Hero works, ask for **About**, then **Projects**, then **Contact** in separate steps.

**Good habit:** when a section works, **commit** your changes in Git with a short message (your instructor can demo this).

---

## Project layout (cheat sheet)

| Path | Purpose |
| ---- | ------- |
| `src/app/page.tsx` | Main page — you will assemble sections here. |
| `src/app/layout.tsx` | Site-wide shell (title in the tab, fonts, etc.). |
| `src/app/globals.css` | Global CSS (Tailwind is already wired in). |
| `src/components/` | Your section components (Hero, About, …). |
| `src/lib/` | Small shared helpers later if you need them. |
| `.cursorrules` | Hints for the AI about this repo — you usually do not edit this. |

---

## npm commands reference

| Command | When to use it |
| ------- | -------------- |
| `npm install` | First time setup, or after pulling big changes. |
| `npm run dev` | Daily development; local preview at localhost:3000. |
| `npm run build` | Check that the site builds without errors (also what hosting runs). |
| `npm run start` | Run the production build locally (after `npm run build`). |
| `npm run lint` | Check code style / common issues. |

---

## Deploying to Vercel (when you are ready)

[Vercel](https://vercel.com) is made by the same team behind Next.js and works well for this project.

1. Push your code to GitHub (or Git provider your class uses).
2. Sign in to Vercel and **Import** that repository.
3. Keep the default **Next.js** settings and deploy.

You will get a **public URL** to share.

---

## Stretch goals (if you finish early)

Pick any:

- Dark mode toggle  
- Smooth scroll between sections  
- A simple animation when the page loads  
- Polish typography and spacing  

---

## Quick troubleshooting

| Problem | What to try |
| ------- | ----------- |
| `command not found: npm` | Install Node.js and restart the terminal. |
| Port 3000 already in use | Stop another app using that port, or run `npx next dev -p 3001` and open port 3001. |
| Blank page or red error overlay | Read the error text; copy it into Cursor chat and ask what it means. |
| Changes not showing | Save the file; confirm `npm run dev` is still running. |

---

You are set. **Install → clone → `npm install` → `npm run dev` → talk to Cursor.** Good luck, and have fun shipping your first portfolio.
