% README.tex
% Určené pre GitHub repozitár – kompilovať pomocou pdflatex alebo lualatex

\documentclass[12pt, a4paper]{article}

% --- Packages ---
\usepackage[T1]{fontenc}
\usepackage[utf8]{inputenc}
\usepackage[english, slovak]{babel}   % posledný jazyk = hlavný
\usepackage{geometry}
\usepackage{hyperref}
\usepackage{enumitem}
\usepackage{booktabs}
\usepackage{parskip}
\usepackage{titlesec}
\usepackage{xcolor}

\geometry{margin=2.5cm}

\hypersetup{
    colorlinks=true,
    linkcolor=blue,
    urlcolor=blue,
    pdfauthor={Samuel},
    pdftitle={Mobile Network Signal Measurement (4G)},
}

% --- Title ---
\title{\textbf{Mobile Network Signal Measurement (4G)}\\[0.4em]
       \large Meranie mobilného signálu (4G)}
\author{}
\date{}

% ============================================================
\begin{document}
\maketitle
\tableofcontents
\newpage

% ============================================================
\section*{English Version}
\addcontentsline{toc}{section}{English Version}

% ---- Overview -----------------------------------------------
\subsection*{Overview}
\addcontentsline{toc}{subsection}{Overview}

This repository contains the dataset and interactive map visualizations from a bachelor's thesis
focused on analyzing the coverage and quality of mobile networks (4G~LTE).
The primary focus of this research is measuring signal attenuation (penetration loss) caused by
the physical construction of various public transport vehicles (trains, trams) and evaluating the
impact of measurement equipment placement on GNSS accuracy and Radio Frequency (RF) metrics.

% ---- Measured Routes ----------------------------------------
\subsection*{Measured Routes \& Scenarios}
\addcontentsline{toc}{subsection}{Measured Routes \& Scenarios}

The data logs cover over \textbf{900~kilometres} of railway and road corridors, including:

\begin{itemize}[leftmargin=1.5em]
    \item \textbf{Railway Corridors (CZ):} Prague~-- Cheb, Prague~-- České Budějovice,
          Prague~-- Děčín.
    \item \textbf{Road/Highway Corridors (CZ/SK):} Brno~-- Žilina (and return trips).
    \item \textbf{Urban Public Transport:} Tram lines in the city of Brno
          (e.g.\ historical centre to Technology Park).
    \item \textbf{Specific Scenarios:} Direct comparisons of signal penetration between
          older train carriages and modern units (Moravia) equipped with laser-treated
          metallised windows, as well as testing hardware placement
          (dashboard vs.\ glovebox).
\end{itemize}

% ---- Data Structure -----------------------------------------
\subsection*{Data Structure \& Log Files}
\addcontentsline{toc}{subsection}{Data Structure \& Log Files}

The raw data is provided in \texttt{TXT/CSV} format, collected using the
\textbf{G-NetTrack Pro} diagnostic application.

\subsubsection*{Glossary of Log File Abbreviations}

\begin{description}[leftmargin=2em, labelindent=0em]
    \item[\texttt{Timestamp}] Date and exact time of the logged measurement.
    \item[\texttt{Longitude / Latitude}] GNSS spatial coordinates.
    \item[\texttt{Speed}] Speed of the device/vehicle (km/h).
    \item[\texttt{Network Tech / NetworkMode}] The active radio technology (e.g.\ 4G).
    \item[\texttt{Node / CellID / LAC}] Identifiers for the connected cell tower and location area.
    \item[\texttt{NodeLevel (RSRP)}] Reference Signal Received Power (in dBm).
          The primary indicator of signal strength.
    \item[\texttt{Qual (RSRQ)}] Reference Signal Received Quality (in dB).
    \item[\texttt{SNR (SINR)}] Signal-to-Interference-plus-Noise Ratio (in dB).
          A critical parameter for data throughput and connection quality.
    \item[\texttt{LTERSSI}] Total received signal strength indicator,
          including noise and interference.
    \item[\texttt{Accuracy}] GNSS localisation accuracy (in metres).
    \item[\texttt{Altitude / Height}] Elevation data.
\end{description}

% ---- MATLAB -------------------------------------------------
\subsection*{MATLAB Visualisations}
\addcontentsline{toc}{subsection}{MATLAB Visualisations}

In addition to raw logs, this repository includes MATLAB files used for data post-processing
and spatial visualisation. You can download these files, run them in your local MATLAB
environment, and interact with the maps (zoom in on specific streets, pan across the railway
corridors, and inspect the precise handover points and signal drops).

% ============================================================
\newpage
\begin{otherlanguage}{slovak}

\section*{Slovenská verzia}
\addcontentsline{toc}{section}{Slovenská verzia}

% ---- O projekte ---------------------------------------------
\subsection*{O projekte}
\addcontentsline{toc}{subsection}{O projekte}

Tento repozitár obsahuje namerané dáta a interaktívne mapové vizualizácie z bakalárskej práce
zameranej na analýzu pokrytia a kvality mobilných sietí (4G~LTE).
Hlavným cieľom tohto výskumu je meranie útlmu signálu spôsobeného fyzickou konštrukciou
rôznych prostriedkov hromadnej dopravy (vlaky, električky) a vyhodnotenie vplyvu umiestnenia
meracej aparatúry na presnosť GNSS a rádiové (RF) parametre.

% ---- Merané trasy -------------------------------------------
\subsection*{Merané trasy a scenáre}
\addcontentsline{toc}{subsection}{Merané trasy a scenáre}

Dátové logy pokrývajú viac ako \textbf{900~kilometrov} železničných a cestných koridorov,
vrátane:

\begin{itemize}[leftmargin=1.5em]
    \item \textbf{Železničné koridory (ČR):} Praha~-- Cheb, Praha~-- České Budějovice,
          Praha~-- Děčín.
    \item \textbf{Cestné koridory (ČR/SR):} Brno~-- Žilina (a spiatočné jazdy).
    \item \textbf{Mestská hromadná doprava:} Električkové trate v Brne
          (napr.\ z historického centra do Technologického parku).
    \item \textbf{Špecifické scenáre:} Priame porovnania priestupnosti signálu medzi
          staršími vagónmi a modernými jednotkami (Moravia) s pokovovanými oknami,
          ako aj testovanie umiestnenia hardvéru v aute
          (palubná doska vs.\ odkladacia priehradka).
\end{itemize}

% ---- Štruktúra dát ------------------------------------------
\subsection*{Štruktúra dát a log súbory}
\addcontentsline{toc}{subsection}{Štruktúra dát a log súbory}

Surové dáta sú poskytované vo formáte \texttt{TXT/CSV} a boli zbierané pomocou
diagnostickej aplikácie \textbf{G-NetTrack Pro}.

\subsubsection*{Vysvetlivky skratiek v log súboroch}

\begin{description}[leftmargin=2em, labelindent=0em]
    \item[\texttt{Timestamp}] Dátum a presný čas zaznamenania hodnoty.
    \item[\texttt{Longitude / Latitude}] Priestorové GNSS súradnice
          (zemepisná dĺžka a šírka).
    \item[\texttt{Speed}] Rýchlosť pohybu zariadenia/vozidla (km/h).
    \item[\texttt{Network Tech / NetworkMode}] Aktuálne využívaná rádiová technológia
          (napr.\ 4G).
    \item[\texttt{Node / CellID / LAC}] Identifikátory pripojenej základňovej stanice
          a lokality.
    \item[\texttt{NodeLevel (RSRP)}] Sila prijatého referenčného signálu (v~dBm).
    \item[\texttt{Qual (RSRQ)}] Kvalita prijatého referenčného signálu (v~dB).
    \item[\texttt{SNR (SINR)}] Odstup užitočného signálu od šumu a interferencií (v~dB).
          Kritický QoS parameter.
    \item[\texttt{LTERSSI}] Celková úroveň prijatého signálu vrátane šumu a rušenia
          z~okolia.
    \item[\texttt{Accuracy}] Presnosť priestorovej lokalizácie GNSS (v~metroch).
    \item[\texttt{Altitude / Height}] Údaje o~nadmorskej výške.
\end{description}

% ---- MATLAB -------------------------------------------------
\subsection*{MATLAB vizualizácie}
\addcontentsline{toc}{subsection}{MATLAB vizualizácie}

Okrem surových logov tento repozitár obsahuje aj MATLAB súbory využité na post-processing
a priestorovú vizualizáciu dát. Tieto súbory si môžete stiahnuť, otvoriť vo svojom lokálnom
prostredí MATLAB a s mapami priamo interagovať (približovať konkrétne ulice, posúvať sa po
trati a detailne skúmať body handoveru či výpadky signálu).

\end{otherlanguage}

\end{document}
