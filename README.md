### Wichtig ###
* Compiler --> XeLaTeX
* Compilierfolge: XeLaTeX --> Bib(la)tex --> XeLaTeX --> XeLaTeX
* An Main Datei nur Includierung ändern!

Dies Bitte beachten!

### Konventionen ###
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
### Anleitung ###
Im Folgenden eine kleine Anleitung für LaTeX:
Im Grunde ist der Syntax recht einfach. Um text zu erzeugen muss man ihn einfach nur eingeben. Dennoch ist es wichtig einiges zu beachten.
Da ich das Hauptdokument mit Präambel schon erstellt habe hier einfach die Basics.
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