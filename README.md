# Smart Code Analyzer & CPU Execution Simulator

A deployable, browser-based academic project integrating three subjects:

- **FLAT (Modules 1–2):** token recognition, finite-state-style classification, and regular-expression testing.
- **COA (Modules 1–2):** CPU registers, arithmetic instructions, and the fetch–decode–execute cycle.
- **DAA (Modules 1–2):** linear vs. binary search, comparison counts, Big-O complexity, and merge sort.

## Run locally

No dependencies or build step are required.

1. Download and extract this project.
2. Open `index.html` in Chrome, Firefox, Edge, or Safari.

Or run a local static server from this folder:

```bash
python3 -m http.server 8000
```

Then visit `http://localhost:8000`.

## Deploy online

### Option A — Netlify (easiest)
1. Open https://app.netlify.com/drop
2. Drag the extracted project folder (containing `index.html`) into the drop area.
3. Netlify will publish it and provide a public URL.

### Option B — Vercel
1. Push this folder to a GitHub repository.
2. In https://vercel.com, choose **Add New → Project** and import the repository.
3. Use these settings:
   - Framework preset: **Other**
   - Build command: leave empty
   - Output directory: `.`
4. Deploy.

### Option C — GitHub Pages
1. Push `index.html` to the root of a GitHub repository.
2. Open **Settings → Pages**.
3. Under Build and deployment, select **Deploy from a branch**, choose your branch and `/ (root)`, then Save.

## Features

1. **Code Tokenizer** — classifies keywords, identifiers, numeric literals, operators, and delimiters. Unknown characters are marked.
2. **Pattern Matcher** — tests an input against a regular expression and reports invalid expressions.
3. **Algorithm Complexity Lab** — compares linear search and binary search by comparison count. Binary search operates on a sorted copy.
4. **CPU Instruction Simulator** — runs one instruction per line:
   - `LOAD R1, 5`
   - `ADD R1, 3`
   - `SUB R1, 1`
   - `MUL R1, 2`
   - `STORE R1, result`
5. **Merge Sort Demo** — shows split/merge steps, sorted output, comparison count, and complexity.

## Example CPU program

```text
LOAD R1, 5
ADD R1, 3
MUL R1, 2
SUB R1, 4
STORE R1, result
```

Expected final register value: `12`.

## Important scope note

This is a teaching prototype, not a production compiler or cycle-accurate CPU emulator. The tokenizer recognizes a small subset of C-like syntax. The application runs entirely in the browser and does not collect or transmit user data.

## Suggested presentation split

- Member 1: FLAT — tokenization and regular expressions.
- Member 2: COA — registers and instruction execution.
- Member 3: DAA — search comparison and merge sort.
- Member 4 (if applicable): testing, integration, deployment, and future improvements.
