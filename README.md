# research-loops

Small collection of single-file static tools for screening and reviewing Federal Register documents.

Summary
- `index.html` — placeholder stub (contains the text `hello`).
- `federal-register/index.html` — a standalone static "research loop" UI that searches the Federal Register and uses the Anthropic API to score and summarize results.
- `federal-register/app-1/index.html` — a separate single-file app titled "Should I read this?" that takes a corpus (CSV/JSON or text files), sends one call per document to an Anthropic model to keep/cut each document, and displays the reasons and evidence.

Key points
- These are pure static HTML files (CSS + JS embedded). There is no backend included in this repo.
- Each page runs entirely in the browser with your own Anthropic API key. See the comment block at the top of each HTML file for its Content-Security-Policy and optional full-text proxy details.

Running locally
1. Open a terminal in this folder.
2. Start a simple static server (this avoids file:// CORS issues):

```bash
python3 -m http.server 8000
```

3. Visit `http://localhost:8000/` and open the files:
- `federal-register/index.html`
- `federal-register/app-1/index.html`
