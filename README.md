# latex-in-hindi
For creating latex document in the Hindi language over Overleaf. I have used polyglossia package and changed language settings for Hindi. And used \renewcommand to change the Arabic page numbering in Devanāgarī. 

## Highlights
#### Page numberig appears in Devanāgarī.
#### Equation Numbering and Image numbering appears in Devanāgarī.
#### Section Numbering appears in Devanāgarī.


See the [PDF](https://github.com/nishantaMishra/latex-in-hindi/main.pdf )


## How to use
Start any project on Overleaf and insert the `devanagariNumbering.tex` file in the root directory and call it in the preamble of your main.tex using the command `\input{devanagariNumbering}`

Minimum required configuration:

```latex
%%%%%%%% preamble %%%%%%%%
\usepackage{fontspec} 
\usepackage{polyglossia}
\usepackage{fancyhdr}
\usepackage{amsmath}
\usepackage{afterpage}
\usepackage[T1]{fontenc}
\usepackage{enumitem}
\usepackage{pifont}

% Set Devanāgarī fonts
\newfontfamily\devanagarifont[Script=Devanagari]{Shobhika} % Main Devanāgarī font
\newfontfamily\devanagarifontsf[Script=Devanagari]{Shobhika} % Sans-serif Devanāgarī font
\setmonofont{Noto Sans Devanagari} % For \texttt{} in Devanāgarī

% Set the main language and fonts
\setmainlanguage[numerals=Devanagari]{hindi}
\setmainfont{Shobhika}
\newfontfamily\englishfont[]{Times New Roman}

\input{devanagariNumbering}

\begin{document}

%%%%% Table of Contents %%%%%
\clearpage
\renewcommand{\contentsname}{विषयानुक्रमणिका}
\pagestyle{empty}
\tableofcontents
\clearpage

%%%%% Pagenumbering %%%%%
\pagenumbering{arabic}
\pagestyle{fancy}

%%%%%%%% Rest of the document %%%%%%%%
```

## Project Files

- **`devanagariNumbering.tex`**: Main configuration file containing macros for converting all numbering (pages, sections, equations, figures) to Devanāgarī numerals.
- **`devanagariNumbering2.tex`**: Alternative version of the numbering configuration.
- **`main.tex`**: Main document file.
- **`01_CoverPage.tex`**: Cover page configuration.
- **`README.md`**: This documentation file.

```