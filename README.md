# Data Model Terminology

This repo publishes the words Laerdal agreed for simulation assessment data, and marks which of them are data products. It is the master copy: every wording change starts here.

- **The page:** [laerdal-medical.github.io/proddata-terminology](https://laerdal-medical.github.io/proddata-terminology/) shows the terms in three views. It opens without a login.
- **terms.md:** the terms as plain text, with their definitions.
- **word-list.md:** the code names the terminology Claude skill flags, and the approved name it suggests for each.

The terminology skill reads [terms.md](https://raw.githubusercontent.com/Laerdal-Medical/proddata-terminology/main/terms.md) and [word-list.md](https://raw.githubusercontent.com/Laerdal-Medical/proddata-terminology/main/word-list.md) on every run. A change merged here changes what the skill says, with no change to the skill.

## How to change a term

1. **New or changed definition:** edit terms.md.
2. **A code name the skill should flag:** add a row to word-list.md.
3. **A removed term:** delete it from terms.md, and delete its rows in word-list.md.
4. Open a pull request. Someone other than you approves it before it merges.
5. Tell the Product Data team when a definition changes. The page holds its own copy of the definitions and needs a separate update.

[CLAUDE.md](CLAUDE.md) gives the full rules, written for a Claude agent working in this repo.

An internal copy of the page, for Laerdal GitHub users, lives in `Laerdal-Medical/proddata-data-products` as `simulation-terminology.html`.
