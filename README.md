# UK Academic Format Checker

An AI Skill that checks UK university coursework, essays and dissertations against the student's actual assignment brief, handbook, template and institution-specific referencing guide.

## Why I Built This

While studying in the UK, I found that students frequently struggled with academic formatting and referencing requirements.

The main difficulty was not simply “how to use Harvard referencing”. Different universities, departments and modules may use different Harvard variants, word-count rules, submission templates and formatting requirements.

Most existing tools provide generic citation advice, but cannot determine whether a document follows the requirements of a specific course.

This project was created to turn scattered academic guidance into a clear, source-based checking workflow.

## What It Does

The Skill can help students:

- Extract formatting requirements from assignment briefs and handbooks
- Identify the required referencing style and version
- Check in-text citations against the reference list
- Review headings, layout, word-count rules, figures and tables
- Distinguish confirmed errors from issues requiring further verification
- Produce prioritised and actionable correction suggestions
- Create a corrected editable copy when requested

## How It Works

1. Collect the assignment brief, module handbook, referencing guide and draft
2. Identify which document has the highest authority
3. Extract explicit requirements into a structured checklist
4. Compare the draft against those requirements
5. Classify findings as:
   - Confirmed mismatch
   - Possible issue requiring verification
   - Cannot be checked with the available files
6. Return prioritised corrections with locations, rules and confidence levels

## Key Product Decisions

### Institution-specific checking

The Skill does not assume that all UK universities use the same Harvard referencing style. It treats the student's official module and university guidance as the primary source of truth.

### No fabricated reference information

Missing authors, dates, page numbers, DOIs and URLs are flagged for verification rather than generated automatically.

### Traceable feedback

Each issue is linked to its location, the applicable requirement and a proposed correction, allowing students to understand why a change is needed.

## Example Prompt

> My university requires Harvard referencing. Please compare my essay with the assignment brief and department referencing guide, then check the citations, reference list, word-count rules and document layout.

See [example-prompt.md](./example-prompt.md) for a complete example.

## Example Output

The Skill returns:

- A requirements summary
- A prioritised issue table
- Before-and-after correction examples
- A list of requirements that still need confirmation
- A clear distinction between confirmed errors and uncertain issues

See [example-output.md](./example-output.md) for the output structure.

## Repository Structure

- `SKILL.md` — Core Skill instructions and checking workflow
- `example-prompt.md` — Example user request
- `example-output.md` — Example response structure
- `LICENSE` — MIT License

## Limitations

- The Skill cannot guarantee compliance without the official course documents
- It does not verify whether a cited source genuinely exists unless the original source is provided
- It supports formatting and referencing checks, rather than replacing academic judgement or writing the student's assignment

## Status

Version 1.0 — Initial public release
