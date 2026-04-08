# Project Contract

## Project Overview

GitHub profile README repository (`Angh84/Angh84`). Displays WakaTime developer activity metrics on the GitHub profile page via automated daily updates.

## Architecture

- `README.md` — Profile page. Contains `<!--START_SECTION:waka-->` / `<!--END_SECTION:waka-->` block auto-populated by the WakaTime action.
- `.github/workflows/waka-readme.yml` — GitHub Actions workflow using `athul/waka-readme@master`. Runs daily at 04:00 UTC and on manual trigger. Requires `WAKATIME_API_KEY` secret.

## Reference Files

- `doc/labels.md` — standardized GitHub issue labels (shared across all personal repos)

## Key Constraints

- The WakaTime block in README.md is machine-generated — never hand-edit content between the waka section markers.
- Workflow config (block characters, display toggles) lives in the workflow YAML, not README.md.
- Most commits are automated by `github-actions` bot. Manual commits are rare.

## User Preferences

- Ask first when something important is unclear or uncertain.
- Establish a clear plan before substantive work.
- Do not add `Co-Authored-By` trailers to commit messages.
- Disagree when wrong. State the correction directly.
- Do not change a correct answer because the user pushes back.
- If unsure: say "I don't know." Never guess confidently.
- Never speculate about code, files, or APIs you have not read.
- If referencing a file or function: read it first, then answer.
- Never invent file paths, function names, or API signatures.

## Safety Rails

### NEVER
- Edit content between `<!--START_SECTION:waka-->` and `<!--END_SECTION:waka-->` markers
- Remove or rename the `WAKATIME_API_KEY` secret reference
- Change the workflow schedule without explicit approval

### ALWAYS
- Verify workflow YAML syntax after edits
- Preserve the waka section markers in README.md
