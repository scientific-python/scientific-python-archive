---
theme: metropolis
title:  Scientific Python Ecosystem Coordination \newline \hspace{5cm} SPEC documents
subtitle: SciPy 2021 \newline
  \small July 14, 2021
author: K. Jarrod Millman \& Stéfan van der Walt \newline
  \small University of California, Berkeley
header-includes:
    - '\makeatletter'
    - '\beamer@ignorenonframefalse'
    - '\makeatother'
    - \usepackage{listings}
    - \usepackage[round]{natbib}
    - \usepackage{ragged2e}
    - \usepackage{array}
    - \input{macros}
    - \setbeamertemplate{frametitle continuation}{}
    - \linespread{1.0}
    - \usepackage[cal=cm]{mathalfa}  #stick with the classical Computer Modern \mathcal
    - \usetikzlibrary{decorations.pathreplacing}
    - \newcommand{\highlight}[1]{\colorbox{green!10}{$\displaystyle#1$}}
    - \DeclareMathOperator*{\minimize}{minimize}
    - \DeclareMathOperator*{\maximize}{maximize}
    - \DeclareMathOperator*{\st}{subject\ to}
    - \usepackage{smartdiagram}
    - \usepackage{multirow}
    - \AtBeginSection[]{\begin{frame}{Outline} \tableofcontents[currentsection]\end{frame}}
---

## https://scientific-python.org

\includegraphics[width=\textwidth]{_static/banner.png}

<!--
To better coordinate the ecosystem and prepare scientific Python for the next
decade of data science, we will:
-->

Aims:

#. Create a \textbf{mechanism for} establishing \textbf{community-wide policies},
#. Improve \textbf{common engineering infrastructure},
#. Organize a \textbf{series of developer events} to discuss needs,
#. Write a \textbf{community vetted strategic plan}, and
#. Help the \textbf{community develop grant proposals}.

\vspace{.5cm}

\tiny This work is funded in part by the Gordon and Betty Moore Foundation through grant GBMF8599 to the University of California, Berkeley.

## 

\LARGE \textbf{Aim 1:}

A mechanism for establishing community-wide policies

## https://scientific-python.org/specs

\begin{center}
\vspace{.5cm}
\includegraphics[height=0.85\textheight]{_static/specs-site-emulated.png}
\end{center}

## https://discuss.scientific-python.org

\begin{center}
\vspace{.5cm}
\includegraphics[height=0.85\textheight]{_static/discuss-emulated.png}
\end{center}

## https://github.com/scientific-python/specs

\begin{center}
\vspace{.5cm}
\includegraphics[height=0.85\textheight]{_static/specs-repo.png}
\end{center}

## SPEC Steering Committee

\begin{center}
\vspace{.5cm}
\includegraphics[height=0.85\textheight]{_static/steering-committee.png}
\end{center}

## SPEC Core Projects

\begin{center}
\vspace{.5cm}
\includegraphics[height=0.85\textheight]{_static/core-projects.png}
\end{center}

----

\begin{center}
\LARGE{\textbf{Forum:} \url{https://discuss.scientific-python.org}}

\LARGE{\textbf{Read more:} \url{https://scientific-python.org}}
\end{center}
