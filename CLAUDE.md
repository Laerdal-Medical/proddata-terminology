# CLAUDE.md

This repo is the master copy of Laerdal's simulation assessment terminology. Read this file before you change anything here.

## How the files fit together

- **terms.md:** the approved terms and their definitions. The terminology skill reads it to explain a flag.
- **word-list.md:** the code names the skill flags, and the name it suggests for each. The skill reads it on every run.
- **index.html:** the public page. It reads terms.md every time it opens, so a definition change shows on the page with no edit to index.html. The page decides only where each term sits in its three views. A new term appears under "New terms" until someone gives it a place in `PLACEMENT` inside index.html.

The terminology skill lives in the `competency-qi-data-model` plugin in `Laerdal-Medical/dp-laerdal-skills`. The skill fetches terms.md and word-list.md from the main branch of this repo on every run, so a merged change reaches every user within five minutes. The skill holds no terms of its own. Change the skill only when the method changes, never to add or remove a term.

## Adding a term

1. Add the term to terms.md, between `<!-- terms start -->` and `<!-- terms end -->`. Give it a `###` heading, or `####` for a subterm, and follow the layout of the terms around it.
2. If code uses other names for the term, add them to word-list.md. Put a name under **Suggest** when it always means this term. Put it under **Ask** when it can mean something else, and write the question the skill should ask.
3. Every suggested name must come from terms.md: the term's data product name where it has one, otherwise the term name in snake_case.

## Removing a term

1. Delete the term from terms.md.
2. Delete every word-list.md row that suggests the term's name. Search word-list.md for that name to find the rows.

## Rules

- Never write a count of terms anywhere. Counts go stale.
- Keep a name out of word-list.md until the team agrees it. The skill flags only names listed there, so an undecided name stays silent.
- Changes go in through a pull request. The main branch needs one approving review from someone other than the author.
- Keep the layout of terms.md: a `###` heading per term, `####` for a subterm, each label in bold followed by a full stop (`**Definition.**`), and the `*Data product: …*` line last. The page reads terms.md by that layout.
- After a definition changes, tell the Product Data team, so they can update the internal copy of the page.
