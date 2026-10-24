# Ai-Experimentation-Sandbox
AI Experimentation Sandbox is devoted to AI engineering research, theory, and hands-on practice.

The repository uses the same uv workspace layout as Python-Experimentation-Sandbox.

```text
Ai-Experimentation-Sandbox/
├── pyproject.toml           # Workspace configuration (Python 3.12+)
├── uv.lock                  # Shared dependency lockfile
├── experiments/             # Multi-file research projects, each with pyproject.toml
├── scripts/                 # Small experiments with a shared workspace environment
│   ├── pyproject.toml
│   └── README.md
└── reports/                 # Research findings and benchmark results
```

## Setup

Install [uv](https://docs.astral.sh/uv/getting-started/installation/), then run:

```bash
uv sync --all-packages
```

Workspace members share the root `.venv` and `uv.lock`.

## Scripts

```bash
uv add --package scripts <dependency>
uv run --package scripts python scripts/<filename>.py
```

## Experiments

Create a project from the repository root:

```bash
uv init experiments/YYYY-MM-DD-lab-subject
```

Projects under `experiments/` are included automatically in the workspace.
Inside an experiment, use `uv add <dependency>` and `uv run main.py`.
Run `uv lock` after changing workspace membership or dependency configuration.

## Naming

Use `YYYY-MM-DD-[type]-[subject]` for scripts and experiment directories:

- `spike`: Time-boxed feasibility investigation.
- `poc`: Proof of concept.
- `bench`: Performance benchmark.
- `lab`: Learning and exploration.

Keep conclusions and benchmark summaries in `reports/`.
