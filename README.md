# Python Copier Template

Reusable Copier template for new Python projects using:

- `uv` for dependency management
- `src/` package layout
- Hatchling builds
- Optional Git-tag-based versions with `hatch-vcs`
- Ruff formatting/linting
- ty type checking
- pytest with coverage
- VS Code/Jupyter notebook support through `ipykernel`

## Use

From anywhere:

```bash
copier copy --vcs-ref=HEAD "JohnnyDecimal/70-79 Projekter/python_template" path/to/new-project
```

Use defaults without prompts:

```bash
copier copy --vcs-ref=HEAD --defaults "JohnnyDecimal/70-79 Projekter/python_template" path/to/new-project
```

```bash 
uvx copier copy \
  --vcs-ref main \
  https://github.com/JeppeBondeBakkensen/python_template.git
```

```bash
cd path/to/new-project
uv sync --dev
uv run ruff check .
uv run pytest
```

## Extras

Generated projects include optional extras:

```bash
uv sync --extra plot
uv sync --extra ml
uv sync --extra torch
uv sync --all-extras
```
