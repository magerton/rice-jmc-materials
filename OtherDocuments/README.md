# Overview

Use [Pandoc](https://pandoc.org/) to compile these documents, which are written in Markdown.

The cover letter must be compiled with [coverletter-template.tex](coverletter-template.tex) in the same folder and the flag `--template=template-letterarticle.tex`

# Using Sublime Text 3 for editing + compiling

A nice text-editor for working with Markdown documents is [SublimeText3](https://www.sublimetext.com/3) with the following packages installed:

- [Package Control](https://packagecontrol.io/installation)
- [MarkdownEditing](https://packagecontrol.io/packages/MarkdownEditing)
- [Pandoc](https://packagecontrol.io/packages/Pandoc)
    + Note, the latest version of Pandoc from <https://github.com/tbfisher/sublimetext-Pandoc> can save `document.md` as `document.pdf` when the `out-local` option is set to `true`. To do this
        1. Add the Github repository `https://github.com/tbfisher/sublimetext-Pandoc` via package control. See [docs](https://packagecontrol.io/docs/usage) for how to add a respository.
        2. Install `sublimetext-Pandoc`, not `Pandoc` via Package Control
        3. For questions, see <https://github.com/tbfisher/sublimetext-Pandoc/issues/63> and <https://github.com/wbond/package_control/issues/1255>
        4. Add the `"out-local": true` option to a PDF document build in `Preferences > Package Settings > Pandoc > Settings - User`. For example, your file might read:

            ```
            {
              "user": {

                // your path here
                "pandoc-path": "C:/Program Files (x86)/Pandoc/pandoc.exe",

                // Pandoc conversions of markdown to other formats
                "transformations": {
                  "coverletter":{
                    "scope": {
                      "text.html": "html",
                      "text.html.markdown": "markdown"
                    },
                    "pandoc-arguments": [
                      "--template=coverletter-template.tex ",
                      "--to=pdf",
                      "--standalone",
                    ],
                    "out-local": true,
                  },
                  "my Microsoft Word": {
                    "scope": {
                      "text.html": "html",
                      "text.html.markdown": "markdown"
                    },
                    "pandoc-arguments": [
                      "-t", "docx",
                      "--filter=pandoc-citeproc",
                    ]
                  },
                  "myPDF": {
                    "scope": {
                      "text.html": "html",
                      "text.html.markdown": "markdown"
                    },
                    "out-local": true,
                    "pandoc-arguments": [
                      "-t", "pdf",
                      "--filter=pandoc-citeproc",
                      // use --latex-engine=engine where engine is
                      // pdflatex|lualatex|xelatex. This may need to be specified with a
                      // full path, e.g. on a mac with BasicTeX
                      // "--latex-engine=/usr/texbin/pdflatex"
                      // or on Windows with MiKTeX
                      // "--latex-engine=C:/Program Files (x86)/MiKTeX 2.9/miktex/bin/pdflatex.exe"
                      // if -o or --output missing, will write to a temporary file
                      // "--output=~/Downloads/output.pdf"
                    ]
                  },
                },
              },
            }
            ```