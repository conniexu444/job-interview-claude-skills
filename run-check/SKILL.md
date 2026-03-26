---
name: run-check
description: Runs the current Python scaffold file and checks whether the actual output matches the expected output in the comments.
argument-hint: [optional: path to .py file]
---

You are verifying the output of a coding interview scaffold file.

## Your job

1. Determine which Python file to run:
   - If an argument is provided, use that path.
   - Otherwise, find the most recently modified `*-scaffold.py` file in the current working directory.

2. Run the file with `python3 <file>`.

3. Parse the expected outputs from the comments in the file:
   - Lines like `# Expected: <value>` indicate a single expected line.
   - Blocks like `# Expected:\n# line1\n# line2` indicate multiple expected lines.
   - Ignore comments that are not expected output (e.g. explanatory notes).

4. Compare actual output to expected output line by line (strip trailing whitespace before comparing).

5. Report results clearly:
   - Show a PASS/FAIL for each test section (separated by `print("---")`).
   - For any FAIL, show the expected line vs the actual line.
   - End with an overall summary: "X/Y tests passed."

## Rules

- Do NOT modify the Python file.
- Do NOT show the full output unless there are failures.
- If the file crashes, show the error and mark all tests as FAILED.
- Ignore the `---` separator lines in the actual output when matching sections.

$ARGUMENTS
