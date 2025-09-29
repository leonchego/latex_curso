# latex_curso

## Introducción

## Mi primer documento

Un documento $\LaTeX$ consta de tres partes principales. 

- Primera linea: Define el tipo de documento y sus características pricipales
- : paquetes y configuraciones
- cuerpo: el contenido del texo

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
\title{My first LaTeX document} %% título del documento
\author{Hubert Farnsworth} %% author
\date{August 2022} %% Fecha

\begin{document}
\maketitle %% añade titulo/author/fecha al documento
Contenido del docuemnto
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
    \caption{A nice plot.}
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
In physics, the mass-energy equivalence is stated by the equation $E=mc^2$, discovered in 1905 by Albert Einstein.
\end{document}
```

```
\documentclass[12pt, letterpaper]{article}
\begin{document}
The mass-energy equivalence is described by the famous equation
\[ E=mc^2 \] discovered in 1905 by Albert Einstein. 

In natural units ($c = 1$), the formula expresses the identity
\begin{equation}
E=m
\end{equation}
\end{document}
```
