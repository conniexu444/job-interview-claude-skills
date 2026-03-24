---
name: scaffold-problem
description: Scaffolds a coding interview problem — creates a new Python file with imports, function signatures, docstrings, and test cases, but leaves the implementation empty for the user to solve.
argument-hint: [problem-file.md or problem description]
---

You are helping scaffold a coding interview problem for the user to solve themselves.

## Your job

Given a problem description (either from a .md file or pasted directly), create a new Python file with:

1. **Imports** — any standard library modules likely needed (e.g. `collections`, `csv`, `io`, `heapq`). Do NOT import third-party libraries unless the problem requires it.
2. **Constants or lookup tables** — only include constants explicitly given in Part 1. Do NOT include data from later parts.
3. **Function signature for Part 1 only** — one function with a descriptive docstring explaining what it should do. Leave the body as just `pass`. Do NOT scaffold later parts.
4. **Test cases for Part 1 only** — at the bottom under `if __name__ == "__main__":`, write concrete test cases with expected output as comments using only examples from Part 1.

## Rules

- Only scaffold Part 1. Later parts are revealed by the interviewer — do not include them.
- Do NOT write any solution logic. Function body must only contain `pass`.
- Do NOT write solution hints in comments or docstrings.
- Do NOT include constants, rates, or lookup tables from later parts — only what Part 1 explicitly requires.
- Keep test cases simple and focused — use small, concrete values so the user can verify by hand.
- Name the output file after the problem .md file if one is provided, replacing `.md` with `-scaffold.py`. If no file is given, ask the user for a filename.
- After creating the file, tell the user: what imports were added and why, what the function is supposed to do, and what the expected test outputs are.

## Input

The user will either:
- Pass a path to a `.md` file: read it first, then scaffold based on its contents
- Paste a problem description directly: scaffold from that

$ARGUMENTS
