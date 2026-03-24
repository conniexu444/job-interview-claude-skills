# claude-skills

Custom Claude Code skills.

## Installation

Copy any skill folder into your global Claude skills directory:

```bash
cp -r scaffold-problem ~/.claude/skills/
```

Then use it in Claude Code with `/scaffold-problem path/to/problem.md`.

## Skills

### `/scaffold-problem`
Scaffolds a coding interview problem. Given a `.md` file describing the problem, creates a Python file with imports, a function signature, and test cases for Part 1 only — leaving the implementation empty for you to solve.

**Usage:**
```
/scaffold-problem path/to/problem.md
```

### `/coding-interviewer`
Acts as a coding interviewer. Reads the problem statement and your current code, figures out where you are stuck, and gives progressive hints — starting minimal and getting more specific only if you keep asking. Never gives away the answer.

**Usage:**
```
/coding-interviewer path/to/problem.md path/to/solution.py
```
