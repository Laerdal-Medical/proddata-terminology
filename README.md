# Data Model Terminology

This repo publishes the words Laerdal agreed for simulation assessment data, and marks which of them are data products. It is the master copy: every wording change starts here.

- **The page:** [laerdal-medical.github.io/proddata-terminology](https://laerdal-medical.github.io/proddata-terminology/) shows the terms in three views. It opens without a login.
- **terms.md:** the terms as plain text, with their definitions.
- **word-list.md:** the code names the terminology Claude skill flags, and the approved name it suggests for each.

The page and the terminology skill both read [terms.md](https://raw.githubusercontent.com/Laerdal-Medical/proddata-terminology/main/terms.md). The skill also reads [word-list.md](https://raw.githubusercontent.com/Laerdal-Medical/proddata-terminology/main/word-list.md). A change merged here shows on the page and in the skill, with no change to either.

## How to change a term

1. **New or changed definition:** edit terms.md.
2. **A code name the skill should flag:** add a row to word-list.md.
3. **A removed term:** delete it from terms.md, and delete its rows in word-list.md.
4. Open a pull request. Someone other than you approves it before it merges.
5. A new term shows on the page under "New terms". Ask the Product Data team to give it a place in the page's views.

[CLAUDE.md](CLAUDE.md) gives the full rules, written for a Claude agent working in this repo.

An internal copy of the page, for Laerdal GitHub users, lives in `Laerdal-Medical/proddata-data-products` as `simulation-terminology.html`.
