SemesterProjects
================

This repository is for bachelor projects and semester projects. These differ from minor project mainly because of the `\documentclass{memoir}`


The structure
-------------

A good idea for bachelor projects (semesterprojects) is keeping a good structure of the document and the files within it.

One way of doing it is as follow:

+ Documents/
	+ Accepttest/
		- Main.tex
		- Preamble.tex
		- AT-Part1.tex
		- AT-Part2.tex
		- ...
	+ Design/
		- Main.tex
		- Preamble.tex
		- D-Part1.tex
		- D-Part2.tex
		- ...
	+ Figures/
		- dummy.png
		- ...
	+ Modules/
		/* This is a submodule - Read later for it */
	+ PreliminaryAnalysis/
		- Main.tex
		- Preamble.tex
		- PA-Part1.tex
		- PA-Part2.tex
		- ...
	+ PilotProject/
		- Main.tex
		- Preamble.tex
		- PP-Part1.tex
		- PP-Part2.tex
		- ...
	+ Report/
		- Main.tex
		- Preamble.tex
		- R-Part1.tex
		- R-Part2.tex
		- ...
	+ RequirementSpecification/
		- Main.tex
		- Preamble.tex
		- RS-Part1.tex
		- RS-Part2.tex
		- ...

It seems like a lot of documents, and check with your supervisor if you actually need all of them!


Main.tex and Preamble.tex
-------------------------

Notice that each folder contains a file called Main.tex and Preamble.tex.
These two files will create the structure needed for each document. You can call them whatever you like, but it's a good start.

The Preamble.tex will contain a list of all the packages you will be using in you LaTeX document.
This will keep you Main.tex file clear to look at.

The Main.tex file will contain a `\documentclass`, a link to the Preamble.tex, and links to all the input wanted in the document including front page, table of contents, table of figures and tables, different chapters and sections, and so on.
This is obtained by using the function `\input{}` and the package [\subfiles](http://www.ctan.org/pkg/subfiles).


Subfiles
--------
With subfiles you can compile a single document, without the rest.
Some may have tried to look at [Wikibooks](http://en.wikibooks.org/wiki/LaTeX/Modular_Documents) and seen the use of `\includeonly{}` but it will be a drag to outcomment all unwanted files.
With subfiles you can compile the document you are in currently.

LatexModules
------------
In the Preamble.tex file you register all the packages, environments and style you want to use in you current document.
This file easily exceeds 200 lines of uncontrollable code.

Also - creating the preamble is what takes the longest time. So this has been done for you as well.
See [LatexModules](https://github.com/Limro/LatexModules).

By dividing what you need in small modules - each a standalone .tex file, you can reuse these for other documents.

These can be added to the Preamble with the `\input{../path/filename}` command.

