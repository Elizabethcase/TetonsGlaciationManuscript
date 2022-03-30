# Contributing to this repo


# Generated citation / reference files

The `output` branch contains files automatically generated by the manuscript build process.
It consists of the contents of the `output` directory of the `main` branch.
These files are not tracked in `main`, but instead written to the `output` branch by continuous integration builds.

## Files

This directory contains the following files:

+ [`citations.tsv`](citations.tsv) is a table of citations extracted from the manuscript and the corresponding standard citations and citation IDs.
+ [`manuscript.md`](manuscript.md) is a markdown document of all manuscript sections, with citation strings replaced by citation IDs.
+ [`references.json`](references.json) is CSL-JSON file of bibliographic item metadata ([see specification](https://github.com/citation-style-language/schema/blob/master/csl-data.json)) for all references.
+ [`variables.json`](variables.json) contains variables that were passed to the jinja2 templater. These variables contain those automatically generated by the manubot as well as those provided by the user via the `--template-variables-path` option.

Pandoc consumes `manuscript.md` and `references.json` to create the formatted manuscript, which is exported to `manuscript.html`, `manuscript.pdf`, and optionally `manuscript.docx`.
