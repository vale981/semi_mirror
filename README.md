#Wichtig #
* Compiler --> XeLaTeX
* Compilierfolge: XeLaTeX --> Bib(la)tex --> XeLaTeX --> XeLaTeX
* An Main Datei nur Includierung ändern!
* nur \emph!
Dies Bitte beachten!
#Konventionen #
Jedes Kapitel/Unterkapitel hat eine eigene Datei, welche der Ordner- und Dateistriktur: /Kaptitel/nnn/nn.tex folgt.
Eingebunden wird über:

```
#!tex

\include{./Kaptitel/nnn/nn.tex}
```
Also z.B. Kapitel 1:
```
#!tex

\include{./Kaptitel/001/10.tex}
```
Kapitel 1.1:
```
#!tex

\include{./Kaptitel/001/11.tex}
```
Jedes Kapitel/Unterkapitel trägt eine Nummer (automatisch...)!
# Anleitung #
Im Folgenden eine kleine Anleitung für LaTeX:
Im Grunde ist der Syntax recht einfach. Um text zu erzeugen muss man ihn einfach nur eingeben. Dennoch ist es wichtig einiges zu beachten.
Da ich das Hauptdokument mit Präambel schon erstellt habe hier einfach die Basics.
###Kapitel
Ein neues Kapitel erstellt man mit:
```
#!tex
\section{NAME}
```
Unterkapitel mit 
```
#!tex
\subsection{NAME}
```

Unterunterkapitel mit 
```
#!tex
\subsubsection{NAME}
```
#Bündigkeit
Der geforderte Blocksatz für die Arbeit ist eingestellt, will man aber die Bündigkeit ändern so nutzt man Folgenden Code:

```
#!tex
%Links
\raggedright{TEXT}
%Rechts
\raggedleft{TEXT}
%Mitte
\centering{TEXT}
```
Möchte man größere Textstellen beeinflussen:

```
#!tex
%Links
\begin{flushleft}
TEXT
\end{flushleft}
%Rechts
\begin{flushright}
TEXT
\end{flushright}
%Mitte
\begin{center}
TEXT
\end{center}
```
#Zeilenumbrüche
Möchte man einen manuellen Zeilenumbruch einfügen so genügen zwei Backslash an dieser Stell: 

```
#!tex

Text\\Text nach Zeilenümbruch
```

#Kommentare
Es gibt zwei Arten von Kommentaren. Den Code Kommentar und den \todo Kommentar.

Code Kommentar:
Dieser Kommentar wird beim Kompilieren nicht beachtet und dient der Leserlichkeit des Textes.
Ich setze für unsere Arbeit einen guten Kommentierstiel voraus.
Kommentiert wird wie Folgt:
```
#!tex
%Kommentar
Unkommentierter Text...
%Kommentar 2
Unkommentierter Text...
%Eine Zeile
%Und die Nächste
Nur so funktionieren mehrzeilige Kommentare!
```

Todo Kommentar:
Der Todo Kommentar wird im Kompilat angezeigt und dient der errinerung.
Der Syntax Lautet so:
```
#!tex
%Normal
TextTextText\todo{Kommentart TEXT}
%Untrennbar mit Wort verbunden
TextTextText~\todo{Kommentart TEXT}
```
Der Todo Kommentar ist nur im Notfall anzuwenden!

#Text hervorheben
Man kann in LaTeX text sehr einfach hervorheben.
Dazu gibt es mehrere Möglichkeiten:

```
#!tex
%Hervorhebung, wenn schrift Normal --> Kursiv, wenn Kursiv --> Normal
\emph{text}
%Fett
\textbf{text}
%Unterstreichen
\underline{text}
%Schreibmaschine
\texttt{text}
```
Wir Nutzen aber nur \emph!