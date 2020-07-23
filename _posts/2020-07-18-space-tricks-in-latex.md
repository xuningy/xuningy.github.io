---
layout: post
title: Space tricks in Latex
snippet: How to adjust/shrink white spaces in latex documents for when you're just one line over the conference page limit
tags: [how-to, latex]
---

Here's a quick guide for a bunch of different ways to adjust white spaces in latex. Instead of relying on `vspace` everywhere for everything to fit in a conference paper, try adjusting the white spaces around typical objects: floats (tables, figures, algorithms), text, and equations.

Most of these are documented extensively in the documentation for the `layout` package, so if you're curious to play around some of their tricks, please read the [user manual](http://ctan.math.washington.edu/tex-archive/macros/latex/contrib/layouts/layman.pdf).



<div class="tip">
Some notes:
<ul>
<li>To visualize the margins of the page, use <code>\usepackage{showframe}</code>.</li>
<li>If you want to change the space locally for a few floats, you can enclose the commands and objects in curly braces as follows:
<pre>
<code>
{
  \renewcommand{\arraystretch}{1.5}
  \begin{table}[h]
  ...
  \end{table}
}
</code>
</pre>
here, your commands will only be applied locally to this one table.
</li>
<li>Don't try to apply any of these tricks until you're done with the paper!</li>
</ul>

</div>


## Text
``` latex
\usepackage[font={footnotesize}]{caption} % reduce caption size
\setlength{\skip\footins}{0.5ex} % distance between text and footer
```

### Lists, etc
``` latex
\usepackage{enumitem} %% include this if you don't already have it
% `noitemsep` removes spaces between items in list
% `nolistsep` removes spaces between the surrounding text to the list.
\setlist[itemize]{noitemsep, nolistsep}

% alternatively, you can be more granular with:
\setlength{\topsep}{0pt} % rubber space between first (or last) item and preceding(or following) paragraph.
\setlength{\parskip}{0pt} % rubber space between paragraphs with an item

```

### Equation
``` latex
% fix equation spacing before and after
\setlength{\abovedisplayskip}{1pt}
\setlength{\belowdisplayskip}{1pt}

```

### Algorithm
If you use the `algorithm2e` package, you can set the font size as follows:
``` latex
\SetAlFnt{\small}
```

## Float environments
Floating environments are figures, tables and algorithms.
The relationship between text and floats are shown in the following image. Changing the macros will affect all types of floats.

{% include image.html url="/assets/2020-07-18-space-tricks-in-latex/layout.png" description="Macros for setting space between floats and surrounding text." width="50%" %}

To change these spaces:
``` latex
\setlength{\floatsep}{0pt}% Remove space between two floats
\setlength{\textfloatsep}{0pt}% Remove space between top/bottom float and text
\setlength{\intextsep}{0pt} % remove space between text and here
\setlength{\tabcolsep}{4.5pt} % reduce horizontal table padding

% for floats that have captions
\setlength{\belowcaptionskip}{0.7em} % reduce space below captions
```

### Tables

``` latex
% Change table row height (this is a factor representing the distance between two rows)
\renewcommand{\arraystretch}{1}   %% 1 is default

% Change table column width (this is half the space between two columns)
\renewcommand\tabcolsep{6pt}      %% 6pt is default

% Fix table caption distance to table
\captionsetup{skip=5pt}           %% space between caption distance to table
```
<br/>

---------------------

## Preset spacing for conference .cls
<div class="danger">
<b>Do not do this unless this is your last resort! Modifying the given .cls is not recommended!</b>
</div>
Conferences usually provide a `.cls` file which encode the format. You may notice that your section titles have large spaces preceding them sometimes, that may be due to the adaptive spacing they encode in for the section titles. I do not recommend changing this, but if-need-be, here's a way to disable the adaptive spacing (and change the fixed spacing) for your paper.

In your `.cls` file, try to find a section that contains `\def\section{@startsection{`. You might see something like this for each type of section definition:

```latex
\def\section{\@startsection{section}{1}{\z@}{1.5ex plus 1.5ex minus 0.5ex}%
{0.7ex plus 1ex minus 0ex}{\normalfont\normalsize\centering\scshape}}%
```

The `0.7ex plus 1ex minus 0ex` is the adaptive spacing. Notice that there are two. One is for before the section title, the other is for after. To remove adaptive spacing, simply remove all text after the first number. You _can_ change the fixed space number also, however I do not recommend this.
