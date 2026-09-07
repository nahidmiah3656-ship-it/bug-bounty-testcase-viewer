# Cybersecurity Test Case Viewer

A React + Vite Markdown documentation viewer for cybersecurity test cases.

## Features

- Uses the exact contents of `public/test-cases.md` as the single source of truth. No test cases are invented, renamed, removed, or rewritten.
- Proper Markdown rendering with GitHub-Flavored Markdown.
- Searchable heading navigation.
- Raw Markdown / rendered view.
- Copyable code blocks.
- Responsive sidebar.
- Dark/light theme.
- Security-focused sanitization.
- Security payloads are displayed as documentation/code instead of being executed.

## Run locally

```bash
npm install
npm run dev
```

Then open the local Vite URL shown in the terminal.

## Build

```bash
npm run build
```

## GitHub

Upload the project files to a repository. Do not commit `node_modules/`.

## Important security note

The application intentionally does not execute HTML/JavaScript contained in the Markdown. Dangerous URL schemes are not allowed by the sanitizer. The CSP also restricts script and resource sources.

For a public deployment, keep the server's security headers enabled and review any future Markdown renderer/plugin changes carefully.
