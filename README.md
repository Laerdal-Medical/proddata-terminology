# Data Model Terminology

This repo publishes the words Laerdal agreed for simulation assessment data, and marks which of them are data products.

- **The page:** [laerdal-medical.github.io/proddata-terminology](https://laerdal-medical.github.io/proddata-terminology/) shows the 18 terms in three views. It opens without a login.
- **terms.md:** the same 18 terms as plain text. The terminology Claude skill reads its definitions from [the raw file](https://raw.githubusercontent.com/Laerdal-Medical/proddata-terminology/main/terms.md), so a change here changes what the skill says.

## Where the wording comes from

The master copy is `notes/terminology.md` in the Product Data team's Competence Charter project. Every wording change starts there. Copy the change into `terms.md` and the page, then run `check_terms.py` in that project to confirm all copies match word for word.

An internal copy of the page, for Laerdal GitHub users, lives in `Laerdal-Medical/proddata-data-products` as `simulation-terminology.html`.
