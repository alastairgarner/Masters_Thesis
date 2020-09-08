# Thesis - Markdown to PDF convert

A repo to build a Master's Thesis, written in Markdown, to PDF.



## Requirements

- [Pandoc](https://pandoc.org/installing.html)
- [Pandoc-crossref](https://github.com/lierdakil/pandoc-crossref/releases)
- XeLaTeX (installed with [TexLive](https://www.tug.org/texlive/))



## Usage

The thesis text is written in 'thesis.md', a markdown file with a yaml header. All edits can be made here and tracked with git.



### Generate PDF

To generate a pdf from our markdown file, we use the pandoc conversion tool. This initially converts the markdown to LaTeX, before generating the final pdf. The conversion can be run with:

```bash
pandoc --defaults option.yaml -o thesis.pdf thesis.md
```

The defaults argument specifies a yaml file that contains the default options for the conversion. These options include filters (pandoc-crossref) and optional styling (header.tex).

The '-o' argument specifies the output file name. The final argument is the input markdown file to be converted. The names of these files can be changed to you own preference.



### Adding Figures

To add figures, standard markdown syntax can be used to link an file in the 'figures' directory.

```markdown
![Figure tilte and caption here.](./figures/file_name.svg){#Figure_Handle}
```

The additional curly brackets allows you to define a custom figure handle which can be referenced for automatic figure reference formatting (enabled by the pandoc-crossref extension).



## Other files



**current-biology.csl**

File indicating the citation style to be used. Alternative style files can be found at [zotero.org/styles](https://www.zotero.org/styles).



**header.tex**

A LaTeX file that is prepended to the converted markdown file, allowing you to load any additional packages, as well as adjust the styling for the text/sections headers/bullet lists/etc.



**lastpage.tex**

An optional lastpage with closing quote.



**library.bib**

A bibtex file containing the citations used in the thesis, exported from a reference manager - Mendeley, in my case.



**pandoc-svg.py**

An option pandoc filter, written in python, that converts svg files to pdf files before they're incorporated into the final thesis pdf. I found this can be useful if the text in your figures starts to render strangely (letter kerning goes all out of whack). Another solution is to change text to paths in your vector image editor of choice (Inkscape/Illustrator/Affinity Designer). Credit to [Jerome Robert](https://gist.github.com/jeromerobert/3996eca3acd12e4c3d40) for this filter.



**titlepage.tex**

A LaTeX file containing the content and styling of your title page. Normally pandoc includes a default titlepage in generating the pdf, but I have suppressed this (with options in header.tex) to allow inclusion of this custom title page.