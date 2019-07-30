# README for hyperref bundle
2018-11-30


## INTRODUCTION


This package is used to emend cross-referencing commands in LaTeX to
produce some sort of \special commands; there are backends for the
\special set defined for HyperTeX dvi processors, for embedded pdfmark
commands for processing by Acrobat Distiller (dvips and dvipsone), for
dviwindo, for pdfTeX, for dvipdfm, for TeX4ht, and for VTEX's pdf and HTML
backends.

Included are:

 1. `hyperef' The main hyperlinking functionality.
 2. `backref' a package by David Carlisle to provide links back from
    bibliography to the main text; these are hypertext links after using
    hyperref.
 3. nameref' a package to allow reference to the *names* of sections rather
    than their numbers.

## DOWNLOAD


`hyperref' is available on CTAN:
  CTAN:macros/latex/contrib/hyperref/
    
Also a ZIP file is provided that contains the files, already sorted
in a TDS tree:
  CTAN:install/macros/latex/contrib/hyperref.tds.zip
    
"CTAN:" means one of the `Comprehensive TeX Archive Network'
nodes or one of its mirrors.  This is explained in
  https://texfaq.org/FAQ-archives
    
The main repository of hyperref is located at github
       https://github.com/ho-tex/hyperref
    

## INSTALLATION


### Installation with ZIP file in TDS format

The ZIP file `hyperref.tds.zip' contains the files sorted
in a TDS tree. Thus you can directly unpack the ZIP file
inside a TDS tree. (See CTAN:tds.zip for an explanation of TDS.)
Example:
```
  cd /...somewhere.../texmf
  unzip /...downloadpath.../hyperref.tds.zip
```
Do not forget to refresh the file name database of this TDS tree,
Example:
```
  texhash /...somewhere.../texmf
```

### Manual installation

 1. Download the hyperref files from CTAN or the TUG server.
    If necessary, unpack them.
 2. If directory `beta' exists, replace the files by the counterparts
    in this directory, if you want to use the latest versions.
 3. Generate the package and driver files:
      tex hyperref.ins
 4. Install the files `*.sty', `*.def', and `*.cfg' in your TDS tree:
      cp *.sty *.def *.cfg TDS:tex/latex/hyperref/
    Replace `TDS:' by the prefix of your TDS tree (texmf directory).
    The exception is bmhydoc.sty, it belongs to the source files
    (TDS:source/latex/hyperref/).
 5. Copy the documentation files to "TDS:doc/latex/hyperref/":
    manual.pdf, README, README.pdf, ChangeLog, ChangeLog.pdf,
    slides.pdf, paper.pdf, options.pdf, hyperref.pdf, backref.pdf,
    nameref.pdf (Also the HTML version of the manual can be put there.)
 6. Update the databases if necessary, eg. for teTeX:
      mktexlsr .../texmf
      
## AUTHORS/MAINTAINERS


 * Sebastian Rahtz (died 2016)
 * Heiko Oberdiek
 * David Carlisle (via GitHub ho-tex origanisation)


## BUG REPORTS


A bug report should contain:

 * Comprehensive problem description. This includes error or
   warning messages.
   * \errorcontextlines=\maxdimen can be added in the TeX code
     to get more informations in TeX error messages.
 * Minimal test file that shows the problem, but does not
   contain any unnecessary packages and code.
 * Used drivers/programs.
 * Version information about used packages and programs.
   * If you are using LaTeX, then add "\listfiles". Then
     a list of version informations is printed at the end
     of the LaTeX run.
 * Please no other files than the minimal test file.
   The other files .log, .dvi, .ps, .pdf are seldom necessary,
   so send them only on request.
    
## Bug address

A bug tracker is available at github:
    https://github.com/ho-tex/oberdiek/issues

Alternatively bug reports can be send to the support group public email list:
 <ho-tex [at] tug [dot] org>
      
## Vietnamese part

Responsible for the Vietnamese translations of the
\autoref names and puvnenc.def are:
  Han The Thanh <hanthethanh [at] gmail [dot] com>
  Reinhard Kotucha <reinhard [dot] kotucha at web [dot] de>
      
## Arabic part

Responsible for the additions to PU encoding for Arabi is
  Youssef Jabri <yjabri [at] ensa [dot] univ-oujda [dot] ac [dot] ma>
      

## KNOWN PROBLEMS


 * (half-done) hyper images (link from thumbnail in text)
 * Relative links are not sorted out or documented well.
   For PDF generation:
   * With baseurl: all links are considered relative to this URL.
   * Without baseurl: a relative link without "file:" can be
     achieved by:
     ```
      \begingroup
        \hypersetup{linkfileprefix={}}%
        \href{../foo/bar.html}{bar.html}
      \endgroup
      ```
 * ...
    

## TODO

 * modules
 * bookmark organisation
 * documentation
 * PDF threads
 * more for PDF forms
   * per object setting
   * vary gap between text and box
 * PostScript driver: the current implementation doesn't relly support
   nested links. The start positions should be remembered in a stack,
   but there are complications with page breaks.
 * ...
    

## VERSIONS IN TEX DISTRIBUTIONS

| TeX Live | hyperref | comment |
| -------- | -------- | ------- |
| TL 2016 |      2016/05/05 v6.83n | (at time of first release) |
| TL 2011 |      2011/04/17 v6.82g | (at time of first release) |
| TL 2010 |      2010/06/18 v6.81g | (at time of first release) |
| TL 2009 |      2009/10/09 v6.79a | (at time of first release) |
| TL 2008 |      2008/08/14 v6.78f | (at time of first release) |
| TL 2007 |      2007/02/07 v6.75r | |
| TL 2005 |      2003/11/30 v6.74m | |
| TL 2004 |      2003/11/30 v6.74m | |
| TL 2003 |      2003/09/15 v6.74i | |
| TL 7  (2002) | 2002/05/27 v6.72r | |
| TL 6b (2001) | 2001/05/26 v6.71g | |
| TL 5d (2000) | 2000/07/02 v6.70m | |
| TL 5c (2000) | 2000/05/08 v6.70f | |
| TL 4  (1999) | 1999/04/13 v6.56 | |
| TL 3  (1998) | 1998/03/25 v6.19 | |
      
