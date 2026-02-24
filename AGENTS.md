## Cursor Cloud specific instructions

This is a minimal Streamlit (Python) application. See `README.md` for standard install and run commands.

### Running the app

```
streamlit run streamlit_app.py --server.headless true --server.port 8501
```

- `--server.headless true` is required in headless/cloud environments to suppress the browser auto-open prompt.
- The app serves on port **8501** by default.
- Add `--server.enableCORS false --server.enableXsrfProtection false` if testing from a proxied/embedded browser context.

### Linting

No dedicated linter config exists in the repo. Use `python3 -m py_compile streamlit_app.py` for syntax checks or `python3 -m pyflakes streamlit_app.py` for basic lint.

### Notes

- The `streamlit` binary installs to `~/.local/bin`; ensure this is on `PATH` (`export PATH="$HOME/.local/bin:$PATH"`).
- No database, no external services, no build step required.
