# latex_curso

## Introducción

## Mi primer documento

Un documento $\LaTeX$ consta de tres partes principales. 

- Primera linea: Define el tipo de documento y sus características pricipales
- Paquetes y configuraciones
- Cuerpo: el contenido del texo

Ejemplo: 

```
\documentclass{article}

%%% paquetes y configuraciones

\begin{document}

Mi primer documento

\end{document}
```
## Segundo documento
 
```
\documentclass[12pt, letterpaper]{article}

%%% paquetes
\usepackage{graphicx} %% insertar imágenes

%% configuraciones
\title{Bibliografía Alexander von Humboldt} %% título del documento
\author{Jaime Ibarra } %% author
\date{Agosto 2022} %% Fecha

\begin{document}

\maketitle %% añade titulo/author/fecha al documento

Alexander von Humboldt, de nombre completo Friedrich Karl Wilhelm Heinrich Alexander
y también conocido en español como Alejandro de Humbold, barón von Humboldt, fue un
naturalista, geógrafo y explorador alemán nacido el 14 de septiembre de 1769 en
Berlín y fallecido el 6 de mayo de 1859 en la misma ciudad.​

\end{document}
```

## Secciones

```
\section{Sección 1}
\subsection{Subsección 1}
```

```
\begin{document}

\maketitle %% añade titulo/author/fecha al documento

\section{Introducción}

Alexander von Humboldt, de nombre completo Friedrich Karl Wilhelm Heinrich Alexander
y también conocido en español como Alejandro de Humbold, barón von Humboldt, fue un
naturalista, geógrafo y explorador alemán nacido el 14 de septiembre de 1769 en
Berlín y fallecido el 6 de mayo de 1859 en la misma ciudad.​

\subsection{Contexto}

Tras la muerte de su padre estudió leyes en la Universidad de Göttingen, como deseaba 
su madre, pero ello no le impidió acudir a las clases de ciencias naturales de Georg 
Forster, que había sido dibujante botánico en la segunda expedición del capitán James
Cook.

\end{document}
```

## Agregar imágen

```
\documentclass{article}
\usepackage{graphicx}
\graphicspath{{images/}}
 
\begin{document}

Este documento contiene una imágen, ver figura \ref{fig:mesh1}

\begin{figure}[h]
    \centering
    \includegraphics[width=0.75\textwidth]{mesh}
    \caption{Descripción de la imágen.}
    \label{fig:mesh1}
\end{figure}
 
\end{document}
```

### listas

```
\documentclass{article}
\begin{document}
\begin{itemize}
  \item primer item
  \item segundo item
\end{itemize}
\end{document}
```

```
\documentclass{article}
\begin{document}
\begin{enumerate}
  \item primer item
  \item segundo item
\end{enumerate}
\end{document}
```

### math

```
\documentclass[12pt, letterpaper]{article}
\begin{document}
In physics, the mass-energy equivalence is stated by the equation $E=mc^2$,
 discovered in 1905 by Albert Einstein.
\end{document}
```

```
\documentclass[12pt, letterpaper]{article}
\begin{document}
The mass-energy equivalence is described by the famous equation
\[ E=mc^2 \]
discovered in 1905 by Albert Einstein. 

In natural units ($c = 1$), the formula expresses the identity
\begin{equation}
E=m
\end{equation}
\end{document}
```
### Tablas

```
\usepackage{booktabs} %% tablas
```

```
\begin{table}[h!]
  \caption{Frequency of Special Characters}
  \label{tab:freq}
  \begin{tabular}{ccl}
    \toprule
    Non-English or Math&Frequency&Comments\\
    \midrule
    \O & 1 in 1,000& For Swedish names\\
    $\pi$ & 1 in 5& Common in math\\
    \$ & 4 in 5 & Used in business\\
    $\Psi^2_1$ & 1 in 40,000& Unexplained usage\\
  \bottomrule
\end{tabular}
\end{table}
```

### Citas

Crear un documento con extensión bib: e.g. sample.bib

```
\usepackage[backend=biber, language=spanish, style=apa]{biblatex}

\addbibresource{sample.bib}
```


```
\cite{}
```

```
\printbibliography
```


```
Descubridor científico del Nuevo Mundo cuyo estudio ha dado a América algo mejor que todos los Conquistadores juntos". Así describió Simón Bolívar al hombre considerado el padre de la geografía moderna universal y, actualmente, el primer ambientalista ya que predijo el cambio climático causado por la acción del hombre \cite{amador-dominguez_neurosymbolic_2024}.
\\

\printbibliography
```


####
Para cita de estilo APA

```
\parencite{}
\textcite{}
```

```
Parencite es similar a cite \parencite{amador-dominguez_neurosymbolic_2024}.
```

```
textcite para citar en forma narrativa, \textcite{amador-dominguez_neurosymbolic_2024}.
```

### Renombrar encavezados

```
%\renewcommand{\figurename}{\textbf{\textit{Figura}}}
%\renewcommand{\tablename}{\textbf{\textit{Tabla}}}
\AtBeginDocument{\renewcommand\tablename{Tabla}}
%\renewcommand{\thetable}{\arabic{chapter}.\arabic{tabla}}   
\renewcommand{\contentsname}{\textbf{Tabla de contenido}}
%\renewcommand{\tableofcontents}{\textbf{\textit{Contenido}}}
%\renewcommand{\refname}{Bibliografía}
%\renewcommand\bibsection{\chapter*{\refname}}
\addto{\captionsspanish}{\renewcommand{\refname}{Bibliografía}}
``

