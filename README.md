# United States Code

[![License: CC0 1.0](https://img.shields.io/badge/License-CC0_1.0-lightgrey.svg)](https://creativecommons.org/publicdomain/zero/1.0/)

The United States Code as Git-versioned Markdown. Every change to federal law is tracked as a Git commit, enabling `git log`, `git blame`, and `git diff` on legislation.

> **Independence disclaimer:** This is an independent community project. It is not affiliated with, endorsed by, or associated with any government agency, employer, or official body.

## What This Repository Contains

Structured Markdown files representing the U.S. Code, organized by Title, Chapter, and Section:

```
title-01/
  chapter-01/
    section-001.md
    section-002.md
title-26/
  chapter-01/
    section-0001.md
    ...
```

Each file includes YAML frontmatter with metadata: title number, section number, chapter, the Public Law it was current through, and classification citation.

## Data Source

All content is derived from the official USLM 2.0 XML releases published by the [Office of the Law Revision Counsel](https://uscode.house.gov/) (OLRC). The transformation is performed by [civic-source/us-code-tracker](https://github.com/civic-source/us-code-tracker).

## How Changes Are Tracked

A weekly automated pipeline checks for new OLRC release points (Public Laws). When new legislation is detected, the pipeline transforms the updated XML and commits the changes here. Each commit message references the specific Public Law: `chore(law): Update to PL XXX-XXX`.

Use standard Git tools to explore legislative history:

```bash
# View the history of a specific section
git log --oneline title-26/chapter-01/section-0001.md

# See what changed in a specific commit
git show <commit-hash>

# Compare two versions
git diff <old-hash> <new-hash> -- title-26/
```

## License

This data is dedicated to the public domain under [CC0 1.0 Universal](LICENSE). You may copy, modify, distribute, and use the data for any purpose, without asking permission.

## Contributing

This repository is maintained automatically by the [us-code-tracker](https://github.com/civic-source/us-code-tracker) pipeline. To report issues with the data or transformation, please open an issue in the [us-code-tracker](https://github.com/civic-source/us-code-tracker/issues) repository.
