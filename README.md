# SignVarTables
Permet de générer le code latex d'un tableau de signe ou de variation directement à partir de son expression.


# Exemple 1 (en python) :

x = symbols('x')
f = sin(7*pi/2) + (cos(7*pi/2))^2
tabs_all(f, Interval(0, 4*pi/7) )


# Exemple 2 (avec pythontex) :

\documentclass[a4paper]{article}

\usepackage{pythontex}
\usepackage{tikz,tkz-tab}

\begin{pycode}
import numpy.random as random
from sympy import *
from signVarTable import tabs_all, tab_var

x = symbols('x')
f = -sin(5*x)
\end{pycode}

\begin{document}

\begin{center}
			\py{tab_var(f,Interval(-pi/a, pi/a), continuous_domain=S.Reals, derivability_domain=S.Reals)}
\end{center}

\end{document}
