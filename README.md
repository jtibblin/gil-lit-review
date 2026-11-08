# Experimental studies on gender-inclusive language: a literature database

This is an open, sortable, non-exhaustive database of empirical and experimental studies on gender-inclusive language in French and other languages, with one row per paper. At the moment, it focuses on studies examining the effects of gender-inclusive forms on gender representation (using for example a sentence-evaluation task) and on reading aspects (using for example eye tracking).

**Browse the database:** https://jtibblin.github.io/gil-lit-review/
**Download the data:** [`data/papers.csv`](data/papers.csv)

[Last updated: November 2026 · Number of papers: N]

## Scope

This database is intended to provide a quick overview of existing empirical studies on gender-inclusive language. The categories are intentionally broad and may therefore be imprecise and subjective (such as the distinction between explicit and implicit methods). All information should be checked against the paper to avoid any misinterpretations.

- **Topic:** Empirical, experimental studies on the processing and interpretation of gender-inclusive forms
- **Languages:** The aim is to include any language, so far only studies on French have been included
- **Types of work:** At the current state, only peer-reviewed articles and conference proceedings are included; preprints and theses excluded
- **Time span:** None specified
- **Inclusion criteria:** Studies which report original data and examine at least one gender-inclusive form. At the moment, only studies focusing on the effects of these forms on gender representation and on reading processes are included.
- **Exclusion criteria:** Theoretical or opinion papers, corpus studies

This is not a systematic review, and it is probably incomplete. Missing papers are welcome (see Contributing).

## Using the website

- Click a column heading to sort. Click again to reverse the order.
- Use the search box to find text in any column.
- Use the dropdowns to filter by language, gender-inclusive forms examined, and so on. For columns with several values per cell, a paper appears if any of its values matches.
- "Download CSV" gives you the full data.

## Columns

Each row is one paper, even if it reports several experiments. If a paper reports findings on both RQ foci (Gender representation and Reading, i.e., Liénardy_2023), it is reported on two lines (one per RQ focus). Several values in one cell are separated by a semicolon and a space (`; `).

| Column | Description | Format / allowed values |
|---|---|---|
| ID | Short unique identifier for the paper | First author_year, with a letter if needed, e.g. `Tibblin_2023b` |
| Authors | All authors | `Last, First; Last, First` |
| Year | Year of publication | Four digits |
| Title | Title of the paper | Free text |
| Journal | Journal, book, or repository | Free text |
| Permalink | Permanent link, preferably the digital object identifier | Full links, e.g. https://doi.org/10.5070/G60111267` |
| Language | Language(s) studied | Language name(s) in English, separated by `; ` |
| Forms examined | Linguistic forms compared in the study | Can be any of the following (examples in quotes): Masculine `joggeurs`; Complete doublets `joggeuses et joggeurs`; Contracted doublets `joggeur-euses`; Neutral forms `groupe de jogging`; Feminine `joggeuses` |
| Examples | Example gender-inclusive stimuli | Free text, separated by `; ` |
| Stimulus presentation | How the stimuli were presented | Isolation (if the stimuli were presented as bare words, e.g. in a lexical decision task) or Context (if the stimuli were part of a text, e.g. in a self-paced reading task) |
| Stereotypes | Stereotypicality of the stimuli used | Can be any of: Feminine; Masculine; Neutral. Leave blank if no decisions were made in relation to gender stereotypeotypicality of the stimuli. |
| RQ focus | The focus of the study | Can be any of: Gender representation; Reading |
| Method | Experimental method | e.g. Sentence-evaluation task; Forced-choice task; Questionnaire; Eye tracking; Self-paced reading; Lexical decision task |
| Method type | Whether the method explicitly or implictly examines the RQ focus | Implicit (e.g. Sentence-evaluation task, eye tracking) or Explicit (e.g. Questionnaire) |
| Sample size | Number of participants | Whole number |
| Participant country of residence | Where participants lived | Country or region names in English |
| Data/code availability | Whether data or code are public | `Yes` or `No`. |
| Data/code link | Link to public data or code | Full link to repository. |
| Key findings | One- or two-sentence summary | Free text, in your own words |
| Notes | Anything else worth flagging | Free text |

### Conventions

- Use English for all category values, with one consistent spelling (for example always `Sentence-evaluation task`, never `Sentence evaluation task`).
- Leave a cell empty when the information is not reported or not applicable. Do not write "N/A".
- Save the file as UTF-8 (in Excel: "CSV UTF-8").
- Keep the header row and the column order unchanged.

## Contributing

Corrections and additions are welcome.

1. **Suggest a paper:** [open an issue](../../issues/new) with the DOI and, if you can, the values for the columns above.
2. **Add it yourself:** fork the repository, add a row to `data/papers.csv` (a spreadsheet program that exports "CSV UTF-8" is the easiest way to avoid formatting errors), and open a pull request.

Every change to the CSV is checked automatically (see below). Please fix any errors it reports before asking for a review.

## Data checks

A GitHub Action (`.github/workflows/validate-csv.yml`) runs `scripts/validate_csv.py` on every change to the data. It checks that:

- the header matches the expected columns;
- every row has the right number of fields;
- required columns are filled in and IDs and DOIs are unique;
- Year, Sample size, and DOI have the right format;
- semicolon-separated cells have no empty items;
- columns with a fixed list of values (such as Forms examined) only use allowed values.

It also warns about placeholder text, stray spaces, and author names not written as `Last, First`. To run it locally: `python scripts/validate_csv.py data/papers.csv`. To change what is checked, edit the settings at the top of the script.

## How to cite

If you use this database, please cite it as:

> [Tibblin, Julia] ([2026]). *[Database title]* (Version [0.1]) [Data set]. GitHub. https://github.com/[jtibblin]/[gil-lit-review]

[If you archive releases on Zenodo, put the DOI here instead.]

Please also cite the original papers when you use their findings.

## License

The data are released under [CC BY NC SA] (see `LICENSE`). [The code in `index.html` and `scripts/` is released under the MIT License.]

## Contact

Julia Tibblin, Laboratoire Parole Langage (Aix-Marseille University - CNRS), jtibblin.github.io
