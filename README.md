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

#Aufzählung
Punkte/Itemize:

```
#!tex

%eine Aufzählung, mit Aufzählungszeichen
\begin{itemize}
\item Das erste Item
\item Das zweite Item
\item Das dritte Item
\end{itemize}
```

Unterpunkte mit Itemize im Itemize:

```
#!tex

\begin{document}
\section{Erste Aufzählung}
Eine mehrfach verschachtelte Aufzählung die beim Programmieren schon fast verwirrend sein kann.
\begin{itemize}
\item Erstes Element
	\begin{itemize}
		\item Nächste Ebene
		\item Item in 2. Ebene
	\end{itemize}
\item Zweites Element
\item Drittes Element
	\begin{itemize}
		\item Die zweite Ebene
			\begin{itemize}
				\item Die dritte Ebene
				\item Item in 3 Ebene
			\end{itemize}
		\item Item in 2. Ebene
		\item Item in 2. Ebene
	\end{itemize}
\item Viertes Element
\item Fünftes Element
\end{itemize}
```
Daraus resultiert:

![itemize.jpg](https://bitbucket.org/repo/RAo6K5/images/287777404-itemize.jpg)

Zahlen/Enumerate:

```
#!tex

%eine nummerierte Aufzählung
\begin{enumerate}
\item Das erste Item
\item Das zweite Item
\item Das dritte Item
\end{enumerate}
```

Unterpunkte Auf gleiche weise wie Itemize.
Wenn Itemize in Enumerate --> Anstriche:

```
#!tex

\begin{enumerate}
    \item Punkt 1
    \item Punkt 2
    \begin{enumerate}
        \item Ebene 2 Punkt1 
        \item Ebene 2 Punkt2
        \begin{enumerate}
            \item Ebene 3 Punkt1 
            \item Ebene 3 Punkt2
	\end{enumerate}
    \end{enumerate}
    \item Punkt 3
\end{enumerate}
```
Daraus resultiert:

![Enumerate.png](https://bitbucket.org/repo/RAo6K5/images/3140275116-Enumerate.png)

#Bibliographie
Nach den basics nun die Créme de la Créme: Die Bibliographie.
Um ein buch zitieren zu können müsst ihr es in die Literaturdatenbank aufnehmen. (bei uns: cool.bib)
Ein Beispiel Eintrag:

```
#!tex

@BOOK{Fritzgerland2001,
  AUTHOR       = "Fitzgerald, B. and Russo, N. and DeGross, J.",
                 %Mehrere Autoren werden mit 'and' eingetragen
  TITLE        = "{R}ealigning {R}esearch and {P}ractice in {I}nformation {S}ystems
                 {D}evelopment: {T}he {S}ocial and {O}rganizational {P}erspective",
  PUBLISHER    = "Kluwer Academic Press",
  YEAR         = "2001",
  ADDRESS      = "Boston",
  NOTE         = "Eine optionale Notiz"
}
```
Ganz oben steht der Biblatex Tag mit dessen hilfe ihr später zitiert. Er liegt meistens in der Form. NachnahmeErsterAutor+Veröffentlichungsjahr vor.
Diese Einträge könnt ihr von [Literatur Generator](http://www.literatur-generator.de/) beziehen.

Zitiert wird bei uns nur mit Fußnote:

```
#!tex

%Zitat, in eckige Klammern: Seitenzahl
\footcite[SEITENZAHL]{Biblatex Tag}

%Für SEITENZAHLf. (z.B. S.23f.)
\footcite[SEITENZAHL\psq]{Biblatex Tag}

%Für SEITENZAHLff. (z.B. S.23ff.)
\footcite[SEITENZAHL\psqq]{Biblatex Tag}
```
So leicht wird Zitiert.
Das Literaturverzeichnis erstellt sich automatisch.
Gutes Gelingen :D