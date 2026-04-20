# Dad Jokes

A chatbot that tells dad jokes. One HTML file, hosted on GitHub Pages, calls OpenAI from your browser. No framework, no backend, no build step.

## Try it

[klodzikowski.github.io/lmt-chatbot](https://klodzikowski.github.io/lmt-chatbot/)

Open the drawer (menu icon, top-left), paste an OpenAI API key, send a message. The key lives in your browser session only.

## Goal: build your own chatbot

Takes about ten minutes. You will end up with your own chatbot at your own URL, doing whatever you want.

### 1. Fork this repo

Click **Fork** (top right of this page). GitHub makes you a copy at `https://github.com/<your-username>/lmt-chatbot`.

### 2. Turn on GitHub Pages on your fork

On your fork, go to **Settings → Pages**. Under "Build and deployment":

- Source: **Deploy from a branch**
- Branch: **main**, folder: **`/ (root)`**

Save. Wait 30 to 60 seconds. Your chatbot is live at `https://<your-username>.github.io/lmt-chatbot/`.

### 3. Edit the code

Three options — pick whichever suits you.

**a. In your browser, no install.** On your fork's main page, press `.` (the period key). GitHub opens a full VS Code in the browser at `github.dev/<your-username>/lmt-chatbot`. Edit `index.html`. Commit from the Source Control panel in the left sidebar.

**b. Locally in VS Code.** `git clone` your fork, open it in VS Code. For instant "save = refresh" feedback, install the **Live Server** extension, then right-click `index.html` → Open with Live Server.

**c. Locally in another IDE.** DataSpell, PyCharm, Sublime, WebStorm, whatever. Any editor that can edit HTML works. Same clone → edit → commit → push flow.

If you have GitHub Copilot set up (free for students via [GitHub Education](https://education.github.com/)), let it do the boring edits: "change the system prompt to a Socratic tutor", "add a dark-mode toggle", "rename the title". That is what Copilot is for.

### 4. Make it yours

The interesting edits in `index.html`:

- `DEFAULT_SYSTEM` — the system prompt. This is the invisible first message that steers every reply. Change it and the chatbot becomes a different chatbot: a research assistant, a thesis coach, a Polish→English translator, a grumpy film critic.
- `<h1>Dad Jokes</h1>` and the placeholder text.
- The `:root` CSS variables at the top of the `<style>` block (colours, spacing).
- The `<option>` list inside `<select id="model">` (swap models in and out).
- Default slider values for temperature, top-p, max tokens.

### 5. Republish

Commit. Push. GitHub Pages rebuilds automatically in 30 to 60 seconds. Refresh your URL. Share the link.

## What the drawer gives you

Click the menu icon top-left:

- OpenAI API key input (stored in browser `sessionStorage`, never committed)
- Model picker, newest first (gpt-5-mini → gpt-3.5-turbo)
- Editable system prompt with Reset
- Temperature, top-p, max-tokens sliders, each with a one-line explainer
- Download the whole conversation as JSON (messages, system prompt, sampling settings, token totals)
- Clear chat
- Reset all

## Run locally without pushing

Sometimes you just want to poke at the file without committing. Open `index.html` directly in a browser, or for hot reload:

```bash
python3 -m http.server 8000
```

Then visit `http://localhost:8000`.
