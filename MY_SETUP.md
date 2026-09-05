# Docling — My Setup & Integration

## Original Project

**Original Repository:** https://github.com/docling-project/docling

**Original Authors / Organization:** Docling Project (IBM)

**License:** MIT License

**My Fork:** https://github.com/gajbhiyes774/docling

> **Open Source Project — Setup & Integration** — Original code, license, attribution preserved. My contribution is local setup, install, and testing.

---

## What This Project Does

Python SDK & CLI for converting PDFs, Office files, HTML, Markdown, audio, images, XML, etc. into a unified `DoclingDocument` for downstream AI workflows (gen AI, RAG).

Includes `docling-slim` (light) + `docling` (full), plus `docling-serve` remote service.

---

## Technologies

Python 3.10+ • Hatchling • Transformers • RapidOCR • Docling Parse

---

## How I Configured It

### 1. Fork & Clone
```bash
gh repo fork docling-project/docling --clone=false
# fork: https://github.com/gajbhiyes774/docling
git clone --depth 1 https://github.com/docling-project/docling.git
git remote add fork https://github.com/gajbhiyes774/docling.git
```

### 2. Install
```bash
pip install docling
# → docling 2.126.0 + docling-slim, transformers, docling-parse, etc.
```

System: Python 3.11 (pip via hermes venv), Windows. No Rust needed.

---

## How I Ran It

```bash
python -c "from docling.document_converter import DocumentConverter; print('import ok')"
# → import ok

docling --help
# → convert, convert-remote commands

# Test conversion
echo "# Hello docling" > C:/Users/HP/docling_test.md
docling convert C:/Users/HP/docling_test.md --to md --output C:/Users/HP/docling_out
# → INFO: Converting... Finished in 0.11 sec
# → Output: C:/Users/HP/docling_out/docling_test.md contains "# Hello docling"
```

---

## Problems Encountered & Solutions

| Problem | Solution |
|---------|----------|
| None — `pip install docling` succeeded | — |
| `/tmp/test_doc.md` not found (Linux path on Windows) | Use Windows path `C:/Users/HP/...` |

**Changes made:** None to source — only this `MY_SETUP.md`.

---

## My Contribution

- [x] Forked via GitHub fork (preserved attribution & MIT)
- [x] Cloned original
- [x] Installed `docling 2.126.0` via pip (verified)
- [x] Tested import + CLI + document conversion (Markdown → Markdown)
- [x] Documented setup

---

## Test Report

| Test | Result |
|------|--------|
| `pip install docling` | ✅ 2.126.0 |
| `from docling.document_converter import DocumentConverter` | ✅ import ok |
| `docling --help` | ✅ |
| `docling convert` (md → md) | ✅ 0.11 sec, output verified |

---

## License Preservation

MIT `LICENSE` retained.

---

## Portfolio Card

**Docling — Open Source Project — Setup & Integration**

- Original: https://github.com/docling-project/docling
- My Fork: https://github.com/gajbhiyes774/docling
- Tech: Python • Document Conversion • AI
- My Work: Fork, pip install, CLI test, documentation
- License: MIT

