# CLAUDE.md

## What this is

A personal scratch repo created 2018-01-16 and untouched since. The default
branch is `master`. Until this file, the whole repo was one file, `README.md`,
385 bytes.

There's no build, no tests, and no project scaffolding. Don't go hunting for a
`.csproj` or a solution file. They were never committed.

## Layout

```
hello-world/
  README.md    heading plus a raw C# console snippet
  CLAUDE.md    this file
```

## Review of the current content

Reviewed 2026-08-20. Prose was checked against the `nexcess-brand` skill
(`content-production-standards.md` and `ai-writing-signs.md`); the code was
read normally.

### Code problems in README.md

- The snippet doesn't compile. Three opening braces (namespace, class, `Main`)
  and only two closing ones. The `namespace HelloWorld` block never closes.
- It isn't in a fenced code block, so GitHub collapses it into one run-on
  paragraph and throws away the indentation a reader needs.
- Trailing whitespace on most lines, plus blank lines wedged between each
  declaration and its opening brace.
- The code has no home. It's pasted into a markdown file, not a `.cs` file, so
  nothing would compile it even after the brace is fixed.

### Prose problems

- "how to get a job an ASP.NET developer" is missing the word "as".
- That string is the only sentence in the repo. It's first person and personal,
  which is fine for a scratch repo with an audience of one. It stops being fine
  if the text ever moves somewhere public, since it says nothing about the work.

### Brand audit result

Clean, mostly because there's nothing to catch. No em-dashes, no "Statement one.
Statement two." pairs, no participial closers, no AI vocabulary cluster, no vague
attribution, no recap closing. The heading is already sentence case. The
over-a-beer test passes for the obvious reason that it's a real person talking to
themselves.

Worth stating plainly: `nexcess-brand` is a voice skill for Nexcess public-facing
copy. This is a 2018 personal C# exercise, so most of the checklist (funnel
stage, personas, citation standards, product naming) has nothing to bite on. The
Nexcess skills library has no code-review skill, and none of the other eight
skills in it apply here either.

## Working here

- Fix the brace first if the goal is running code. Then decide whether the
  snippet should become a real `Program.cs` with a `.csproj` instead of living
  inside a README.
- If it stays in the README, wrap it in a csharp code fence so it renders.
- Keep changes small and obvious. There's no test to tell you when you broke
  something.
