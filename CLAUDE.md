# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with this repository. It documents setup, common commands, and where key files live for the local Orpheus TTS Python project.

## Quick Setup

- Recommended Python: 3.8+ (3.10+ preferred).
- Create and activate a virtual environment, then install dependencies:

```bash
python -m venv .venv
# Windows PowerShell
.venv\Scripts\Activate.ps1
# Windows CMD
.venv\Scripts\activate.bat
# Install requirements
pip install -r requirements.txt
```

## Common Commands

- **Install deps:** `pip install -r requirements.txt`
- **Run demo/example:** `python example.py`
- **Run decoder/generation:** `python decoder.py`
- **Model/format helper:** `python gguf_orpheus.py` (used for gguf-related handling in this repo)
- **Run lint (if installed):** `flake8 .` or use `ruff` if configured
- **Run tests (if present):** `pytest`

## Project Layout & Purpose

- `example.py` - Small demo / entrypoint showing typical usage of the TTS pipeline.
- `decoder.py` - Core decoding/audio generation utilities used by the project.
- `gguf_orpheus.py` - Utilities for working with gguf-format model files (conversion/inspection helpers).
- `requirements.txt` - Python dependencies for the project.
- `README.md` - Higher-level project overview and usage notes.
- `examples/` - Example inputs or usage scenarios.
- `outputs/` - Generated audio and other output artifacts written by the project.
- `LICENSE` - Project license.

## Running Locally (example)

Start a fresh environment and run the example:

```bash
python -m venv .venv
.venv\Scripts\Activate.ps1
pip install -r requirements.txt
python example.py
```

Generated audio and artifacts will typically be written into the `outputs/` directory.

## Notes & Tips

- If you plan to use a GPU-backed runtime, ensure dependencies (like PyTorch) are installed with CUDA support per your platform.
- If you add linters or tests, update `requirements.txt` and this file with the exact commands.
- Consult `README.md` for any project-specific configuration, model weights, or licensing details.

## Contact / Maintainers

See `README.md` for maintainer and contact information.