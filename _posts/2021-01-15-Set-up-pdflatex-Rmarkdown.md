---
title: How to Setup pdflatex for RMarkdown in Ubuntu
author: Victor
categories: [IT, RMarkdown]
tags: [RMarkdown, Latex]
---

If your RStudio cannot find pdflatex when it is trying to knit a pdf, you need to setup for it.

```console
/usr/lib/rstudio/bin/pandoc/pandoc +RTS -K512m -RTS ddd.utf8.md --to latex --from markdown+autolink_bare_uris+tex_math_single_backslash --output ddd.tex --lua-filter /home/victor/R/x86_64-pc-linux-gnu-library/3.6/rmarkdown/rmarkdown/lua/pagebreak.lua --lua-filter /home/victor/R/x86_64-pc-linux-gnu-library/3.6/rmarkdown/rmarkdown/lua/latex-div.lua --self-contained --highlight-style tango --pdf-engine pdflatex --variable graphics --variable 'geometry:margin=1in' 
output file: ddd.knit.md

! sh: 1: pdflatex: not found

Error: LaTeX failed to compile ddd.tex. See https://yihui.org/tinytex/r/#debugging for debugging tips. See ddd.log for more info.
In addition: Warning message:
In system2(..., stdout = if (use_file_stdout()) f1 else FALSE, stderr = f2) :
  error in running command
Execution halted

No LaTeX installation detected (LaTeX is required to create PDF output). You should install a LaTeX distribution for your platform: https://www.latex-project.org/get/

  If you are not sure, you may install TinyTeX in R: tinytex::install_tinytex()

  Otherwise consider MiKTeX on Windows - http://miktex.org

```

RStudio looks for pdflatex from the PATH environment.

So we just need to put the **FOLDER** of pdflatex excutable to PATH environment, such as PATH="/home/victor/local/texlive/2020/bin/x86_64-linux:......"

PATH located in /etc/environment file

just use 

```shell
sudo gedit /etc/environment
```



Restart the PC, then Rstudio should be able to find pdflatex now



In the document of Rstudio, it says that we can specify pdflatex by customizing the RSTUDIO_PDFLATEX environment, but that doesnot work for me anyway.

```
> Sys.getenv("RSTUDIO_PDFLATEX")
[1] "/home/victor/local/texlive/2020/bin/x86_64-linux/pdflatex"
```

