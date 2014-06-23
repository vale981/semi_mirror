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