## Convert to pdf

```bash
pandoc -f markdown --filter pandoc-crossref -H header.tex --pdf-engine xelatex --toc --bibliography library.bib --include-before-body=titlepage.tex -o thesis.pdf thesis.md
```

## Convert to presentation

```bash
pandoc -t revealjs -s myslides.md -o myslides.html -V revealjs-url=https://revealjs.com -V theme=serif --slide-level=2
```

## Stats

https://yatani.jp/teaching/doku.php?id=hcistats:mannwhitney#effect_size

https://indrajeetpatil.github.io/ggstatsplot/articles/web_only/effsize_interpretation.html

https://rcompanion.org/handbook/F_04.html



## Future

Convolutional autoencoder

https://towardsdatascience.com/convolutional-autoencoders-for-image-noise-reduction-32fce9fc1763





# To Do

Quantify rate of change of curve. Basically, time between onset and peak. For the same amplitude of bend, does it take longer for A02?

Venn diagram - different pipelines. Or split bar - one bar for each pipeline, proportion coloured by what it overlaps with. Could vary bar length by sum roll dur.

Background - general discussion of escape elements (C-bend, wiggle, thrash, )

Mention larval area corresponds to contour (cos larvae have volume)

