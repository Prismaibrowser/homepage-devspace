# PRISM AI Browser - Developer Homepage

## Overview
This homepage is intended to run as static files. The AI tools now use Groq only.

## Groq Key Setup
1. Copy [.env.example](c:/Users/MY%20LENOVO%20LOQ/Documents/Projects/homepage-devspace/.env.example) to your local `.env`.
2. Put your key in `GROQ_API_KEY=...`.
3. Open [config-loader.html](c:/Users/MY%20LENOVO%20LOQ/Documents/Projects/homepage-devspace/config-loader.html).
4. Paste the `.env` contents and save.

This stores the key in browser `localStorage` as `PRISM_GROQ_API_KEY`.

## AI Tools
- Writing Assistant
- Language Learning
- Code Explainer
- Code Translator
- Decision Analyzer

These tools use `https://api.groq.com/openai/v1/chat/completions` with `openai/gpt-oss-120b`.

## Static File Notes
- `file://` is supported for the homepage itself.
- Daily quotes fall back to bundled values under `file://`.
- If Groq blocks browser-side requests in your environment, the AI tools will still fail because there is no backend proxy in this repo.

## Troubleshooting
- `Missing Groq API key`: load your key through `config-loader.html`.
- `SES`, `lockdown-install.js`, or `contentscript.js` errors usually come from a browser extension, not this repo.
