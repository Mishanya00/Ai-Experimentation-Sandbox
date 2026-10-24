# Scripts

Use this workspace member for small, focused AI experiments.
Name scripts `YYYY-MM-DD-[type]-[subject].py`.

Run from the repository root:

```bash
uv run --package scripts python scripts/<filename>.py
```

Add shared script dependencies with `uv add --package scripts <dependency>`.
For standalone scripts with inline dependency metadata, use
`uv run scripts/<filename>.py`.
