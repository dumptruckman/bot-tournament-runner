# Domain docs

This is a single-context repository.

## What to read

Before exploring the codebase:

- Read `CONTEXT.md` at the repository root if it exists.
- Read relevant architectural decision records under `docs/adr/` if that directory exists.

Do not report these files as missing or suggest creating them before they are needed. The `domain-modeling` skill creates them when the project establishes domain terms or architectural decisions.

## Layout

```text
/
├── CONTEXT.md
├── docs/
│   └── adr/
└── src/
```

## Use the project's vocabulary

Use terms defined in `CONTEXT.md` in issue titles, proposals, hypotheses, and test names. Do not replace established terms with synonyms.

If a needed concept is absent, reconsider whether it belongs to the domain. If it does, note the gap for the `domain-modeling` skill.

## Respect architectural decisions

Call out any proposal that conflicts with an existing ADR. Do not silently override a recorded decision.
