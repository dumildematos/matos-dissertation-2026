# Dissertation: Overleaf project

Skeleton with the dissertation's sections, appendices, page layout and covers. Grey `[Text to write.]` markers show where text goes.

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
| `chapters/` | One file per numbered section (1 to 7). |
| `tables/` | One file per table, loaded from the chapters. |
| `code/` | One file per code listing, loaded from the chapters and the appendices. |
| `figures/` | Logos, plus one folder per chapter. |
| `backmatter/` | References page and appendices. |
| `references.bib` | Bibliography database (BibTeX, `apalike` style). |

## Adding content

- **Text:** replace `\towrite` in the chapter files.
- **Figures:** upload the image to the chapter's folder in `figures/`, then add `\thesisfigure{figures/ch1/fig-name.png}{Caption.}{fig:name}` to the chapter. Until the file exists, a placeholder box shows its name.
- **Tables:** add a file to `tables/` and load it from the chapter with `\input{tables/tab-1-name}`.
- **Code:** add a file to `code/` and load it with `\lstinputlisting[language=Python,caption={Caption},label=lst:name]{code/listing-1-name.py}`.
- **Citations:** add entries to `references.bib`, cite with `\citep{key}`, and remove the `\nocite` line in `backmatter/references.tex`.
- **Cross-references:** use `Fig.~\ref{fig:name}` or `Table~\ref{tab:name}`. Numbers update on their own.
