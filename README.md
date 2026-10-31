# Dissertation: Overleaf project

Skeleton built from the structure of `content.pdf`: same sections, figures, tables, code listings, annex, page layout and covers. Grey `[Text to write.]` markers show where text goes.

## Open in Overleaf

1. New Project > Upload Project, then choose `overleaf-template.zip`.
2. Menu > Compiler: pdfLaTeX. Main document: `main.tex`.

## Layout

| Path | Contents |
| --- | --- |
| `main.tex` | Document order. Start here. |
| `config/metadata.tex` | Author, title, year, degree, supervisors. The covers and title pages read from this file. |
| `config/preamble.tex` | Packages, page layout, helper commands. |
| `frontmatter/` | Covers, title pages, acknowledgements, abstract, glossary, abbreviations, indexes. |
| `chapters/` | One file per numbered section (1 to 6). |
| `tables/` | One file per table, loaded from the chapters. |
| `code/` | One file per code listing, loaded from the chapters and the annex. |
| `figures/` | Logos, plus one folder per chapter. |
| `backmatter/` | References page and annex. |
| `references.bib` | Bibliography database (BibTeX, `apalike` style). |

## Adding content

- **Text:** replace `\towrite` in the chapter files.
- **Figures:** upload a PNG under the name shown in its placeholder box. The `README.txt` in each figure folder lists the names. For another file type, change the path in the chapter too.
- **Code:** paste the code into the matching file in `code/`.
- **Citations:** add entries to `references.bib`, cite with `\citep{key}`, and remove the `\nocite` line in `backmatter/references.tex`. Citations inside figure captions are plain text for now; replace them with `\citep` once the entries exist.
- **Cross-references:** use `Fig.~\ref{fig:lens-comparison}` or `Table~\ref{tab:ssim-per-scene}`. Numbers update on their own.
