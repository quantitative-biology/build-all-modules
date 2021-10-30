# build-all-modules
Build all five quantitative biology modules into one document

A repository for building the document for our five modules. To build it you need the latest version fo all five `module-X-...` modules (in our quantitative-biology organisation) cloned to your computer. 

This is a simplified version (just what is need to build the document) of https://github.com/quantitative-biology/Advanced_Quant_Bio.github.io . But this one does not yet show the rendered html version.

To build:

In R, from the `build-all-modules/` directory:
 
```
bookdown::render_book("index.Rmd", "bookdown::gitbook")
```

In RStudio, click the render button (not the knitr) button, but you may need to make sure you're in the right place (**Andy thinks - can someomone confirm).

If you get errors such as it not finding an `.Rmd` file, then make sure you've updated (`git fetch` and `git rebase`) for each separate repository called `module-X-...`. 

You'll need to install some R packages for some of the modules, so check the error messages you get.

We should list all required packages in `preamble.Rmd` so that are all loaded up front (and give errors straight away if they need installing).

To colour your text in red, use `r colorize("this text is in red")`, and for other colours do `r colorize("this text is in blue", "blue")` etc. (The function is in `preamble.Rmd` that gets loaded into R when running the full `bookdown`).
