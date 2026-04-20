# LMT Chatbot

A static dad-jokes chatbot for the Class 19 warm-up of the 2 MA LMT Artificial Intelligence course at Adam Mickiewicz University. One HTML file, no framework, no build step, no server. Calls OpenAI from the browser with the user's own API key.

## Live

[https://klodzikowski.github.io/lmt-chatbot/](https://klodzikowski.github.io/lmt-chatbot/)

Paste your OpenAI API key into the field at the top. The key stays in `sessionStorage` and is sent only to `api.openai.com`.

## Developer preview

Append `?dev=1` to the URL — or click **Developer preview** in the footer — to reveal:

- Editable system prompt (with Reset button).
- Model selector (defaults to `gpt-4o-mini`).
- Download the full conversation as JSON (system prompt, model, messages, token totals).
- Clear the chat.
- Running tally of messages and prompt/completion tokens.

Normal users land at the clean view. Students get taught about the dev features once they fork and study the code.

## Student workflow (Class 19, no install)

1. Fork this repo on GitHub (button top right).
2. On your fork, press `.` — GitHub opens a full VS Code in the browser at `github.dev/<your-username>/lmt-chatbot`.
3. Open `index.html`, change `DEFAULT_SYSTEM` near the bottom of the `<script>` (or `h1`, colours, anything else).
4. Commit from the Source Control pane in the left sidebar.
5. Wait ~30–60 seconds. GitHub Pages rebuilds your fork. Refresh `https://<your-username>.github.io/lmt-chatbot/`.

Free, zero install, no Python, no Streamlit account.

## Run locally (if you want instant feedback)

Open `index.html` in a browser directly, or for hot reload:

- VS Code with the **Live Server** extension: right-click `index.html` → Open with Live Server.
- Or `python3 -m http.server 8000` and visit `http://localhost:8000`.

## Historical reference

- `v1/` — the 2025 Streamlit version of this chatbot. Deployed to Streamlit Community Cloud last year; kept here as a snapshot of what the deploy-from-template flow produced. Still runs if you `streamlit run v1/streamlit_app.py`.
