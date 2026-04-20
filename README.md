# LMT Chatbot

Class 19 warm-up for the 2 MA LMT Artificial Intelligence course at Adam Mickiewicz University. Two versions of the Streamlit Community Cloud chatbot template, kept side by side so we can re-run either live in class.

## Versions

- `v1/` — the **2025** vanilla template (dad_jokes), GPT-3.5-Turbo. Imported from [klodzikowski/dad_jokes](https://github.com/klodzikowski/dad_jokes) as a historical snapshot.
- `v2/` — the **2026** LMT fork. Seeded academic-tutor system prompt, `gpt-4o-mini` by default, British English copy, header tuned for the class.

Both apps follow the same pattern: one Python file, session-state message list, one OpenAI call per message. The only thing that changes is the branding and the system prompt.

## Deploy to Streamlit Community Cloud

Both versions deploy the same way. On [share.streamlit.io/new](https://share.streamlit.io/new):

- Repository: `klodzikowski/lmt-chatbot`
- Branch: `main`
- Main file path: `v1/streamlit_app.py` or `v2/streamlit_app.py`

Click Deploy, wait about 90 seconds, paste an OpenAI API key into the running app.

## Run locally

From either `v1/` or `v2/`:

```bash
pip install -r requirements.txt
streamlit run streamlit_app.py
```

Opens at `http://localhost:8501`.

## Related materials

Full course structure in `1 - LMT Course Materials/19 - Agents/2 - Class materials/1 - Simple chatbot in Streamlit/` on the shared drive.
