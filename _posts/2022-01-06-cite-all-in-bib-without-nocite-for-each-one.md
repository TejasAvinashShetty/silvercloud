---
toc: true
layout: post
description: by using nocite in a smart way.
categories: [intro, beginner, latex, tutorial]
title: How to cite all elements in a bibliography
comments: true
hide: false
search_exclude: false
categories: [intro, beginner, latex, tutorial]
---

Say one one has a few  citations and a large no of bib entries are not directly used.
But you **still** want to cite them. So what do you do?

Enter `\nocite{}` But this will force you to copy the keys of every bibentry.
I try to be lazy if possible in such matters, so I tried to find how I could 
avoid the repetitive headache.


Turns,out `\nocite{*}` works perfectly for this.
> I forget  now where I read it, though.

```latex
\documentclass{article}
\usepackage[utf8]{inputenc}

\title{cite-all-in-bib-without-nocite-for-each-one}
\author{Tejas Shetty}
\date{January 2022}

\begin{document}

\maketitle

\section{Introduction}
\cite{khaneja2005optimal}
\nocite{*}
\bibliographystyle{apsrev4-1}
\bibliography{tops-ref}
\end{document}

```

See output [here](https://www.dropbox.com/s/xdu5kgg04oi4a5g/cite_all_in_bib_without_nocite_for_each_one.pdf?dl=0)
and [here](https://github.com/TejasAvinashShetty/silvercloud/tree/master/_posts)

[Overleaf link for this project](https://www.overleaf.com/read/ybmrptdhvzgh)
