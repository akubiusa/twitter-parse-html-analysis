# Copilot review instructions

Follow `AGENTS.md` at the repository root for project structure, commands and conventions. Review checklist:

- Python style: Black (88) and isort formatting, type hints and docstrings on public code, flake8 syntax and undefined-name errors (`E9,F63,F7,F82`).
- Privacy: no personal data in logs, error messages or committed files; no credentials; no real export data (`*.json`, `*.csv`, `*.xlsx`, `*.xls`, `parsed/`, `reports/`, `output/`, `results/`, `downloads/`).
- Error handling: no swallowed exceptions around file I/O, JSON loading or HTML parsing; BeautifulSoup lookups must handle `None`.
- Tests: behavior changes in `src/` need matching tests in `tests/`.
- Compatibility: flag breaking changes to `TwitterDataExtractor`, `VideoMisuseAnalyzer`, `LanguageDetector` or CLI options unless `README.md` is updated.
- Do not flag Japanese keyword lists, Twitter UI strings in regexes, Japanese test fixtures, the Japanese CLI console output, or the `--input`/`--input-dir` alias.

Language: write review comments in English. Documentation, code comments and docstrings, and commit/PR text are English; logs and error messages are English.
