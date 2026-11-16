# IRIS Commercial Model Verification — Notebook Downloads & Dependencies Hub

Everything needed to run and inspect the verification notebooks lives inside this single directory (`notebooks/downloads/`), kept gitignored by `notebooks/.gitignore` so none of the repo's locked `uv.lock` environments (`tests/test_locks.py`) or `perception/models/` folders are mutated.

## Folder Contents

| Path | Purpose |
|---|---|
| `venv/` | Shared Python 3.12 virtual environment (`torch 2.14.1+cu130`, `rfdetr`, `onnx`, `onnxruntime-gpu`, Jupyter kernel `iris-rfdetr-test`) |
| `requirements-notebooks.txt` | Frozen package list installed inside `venv/` |
| `models_cache/` | All downloaded pretrained checkpoints (`RF_HOME`, `ROBOFLOW_HOME`, `HF_HOME`, `TORCH_HOME` point here instead of `~/.cache` or `~/.roboflow`) , not in the repo, should be downloaded explicitly|
| `onnx_exports/` | Exported DeepStream `.onnx` files and generated test `config_infer_*.txt` files |

Delete this entire folder anytime to reclaim all disk space used by the notebooks.
