This is a README file for writing material accessible material in Quarto.

STEPS:

1.  Download RStudio (e.g. https://posit.co/download/rstudio-desktop/).
2.  Go to https://github.com/walben-ali/Quarto_Template.git and download ZIP.
3.  If you have an automatic back up system that updates regularly and the folder is in the remit of this back up, then pause it while making change or rendering, this will speed up the process.
4.  Open Template.Rproj.  On the top right, click on the "Build" tab and "Render Book > All Formats".
5.  All the outputs will be produced in the folder called "docs".

FILES INCLUDED:

- _macros.qmd:  Has all the macros used similarly to LaTeX, make sure to put
  :::{.content-hidden}
  {{< include _macros.qmd >}}
  :::
  at the start of every chapter.

- _quarto.yml:  This is the main file that contains all the necessary preamble, including titles and which chapters toinclude under what part headings as well as the specifications of the outputs.  By default, there should be 4 outputs: html, pdf, docx and epub.

- index.qmd:  This is always the first and main chapter.  Do not change the name of this file, Quarto looks for the index.qmd first.

- styleD.scss:  Style file for the dark theme.

- styleL.scss:  Style file for the light theme.

- "documents" folder:  Has all the PDF files that could be included.

- "figures" folder:  Has all the figures that could be included.

- font-controls.html:  This gives the choice of fint styles and sizes.

- references.bib:  BibTeX file for references.

WHEN EDITING:

- When editing, always start my opening the .Rproj file and then working from there.

- You can add or remove chapters at will, just make sure to include those in the _quarto.yml file.

- Make sure to include the macros line in all chapters that will use them.  When rendering PDF, there will be lots of warnings produced saying that "Macro '\B' already defined, ignoring at line 258 column 1", you can ignore those, it will render fine.

- index.qmd is the main file and should always be the first in the list of chapters.

PUSHING THINGS INTO GITHUB FOR THE FIRST TIME:

- Start a new repository on GitHub (personal or intitutional) and make it public.

- Copy the link provided on the GitHub page.

- In RStudio, go to the "Terminal" tab.

- If this is the first time you are pushing things into this empty page, then input the following commands, pressing enter after each one:

	git init

	git remote add origin PASTE_THE_LINK_FROM_GITHUB_HERE

	git add .

	git commit -m "GIVE A LABEL HERE"

	git push -u origin master

((If the last one does not work, then try replacing the word master with main))

- Refresh the page.

- Go to the "Settings" tab.

- On the left navbar, click on "Pages"

- Under the section called "Branch", click on the dropdown menu labelled "None", click on "master" (or "main") and on the next tab, click on "/docs".

- RECOMMENDED FOR EASE OF ACCESS:  Wait and refresh until a new banner on the top appears that says "Your site is live at LINK", that is the link that will have the html output document.  Copy that link, go to the "Code" tab on the top, on the right under "About", paste the link in the "website section".

PUSHING THINGS INTO GITHUB ANY TIME AFTER THAT:

- In RStudio, go to the "Terminal" tab and input the following commands, pressing enter after each one:

	git init

	git remote show origin ((make sure that this displays the link that it should))

	git add .

	git commit -m "GIVE A LABEL HERE"

	git push -u origin master