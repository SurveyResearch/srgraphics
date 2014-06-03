# Graphics
========

Graphics resources.  Two  (and fuzzy) categories:  drawing, and data representation (plotting).

Also, we have:  graphics 

 * Languages
   * Language implementations
 * Programming libraries and APIs (e.g. Java graphics libraries, OpenGL, etc.)
 * Tools or utilities
 * Applications

This repo focusses on doesn't pretend to be complete; there are just too many languages, tools, etc. out there that count as graphicky (e.g. see [](http://www.geos.ed.ac.uk/homes/hcp/idletc.html), 

## Drawing (vector graphics languages)

Very broadly speaking there are two kinds of (vector) graphics language, those that are based on or influenced by Metafont, and those that are not.  An example of the difference:

  *  \draw (0,0) -- (1,1)    // TikZ expression that draws a line from (0,0) to (1,1):  "--" is the "line" operator.
  *  line(0,0,1,1)           // equivalent plain functional syntax, as in Processing

Generally speaking the Metafont syntax is more elegant and easier to work with.  For example, to draw a polyline with Metafont syntax, you just list the sequence of endpoints linked by "--" (which means "line"):  a -- b -- c -- d -- e.  To make this a polygon, you end it with "-- cycle".  Simple, uncluttered, intuitive.  To do the same thing with a plain functional syntax (as in e.g. Processing), you have to write a drawing expression for each segment of the polyline.

Then there's Postscript, which is a stack language with "backwards" syntax - first you write the arguments, then the function name.  It's a great graphics language but virtually nobody writes it by hand.

### Graphics languages and implementations:

#### The TeX legacy:

  * [Metafont](http://en.wikipedia.org/wiki/Metafont).  Metafont was a language specifically designed for font design by Donald Knuth, to complement his [TeX](http://en.wikipedia.org/wiki/TeX) typesetting language/engine.  It isn't used much these days, but it featured a very elegant syntax which has been adopted by several modern general purpose graphics packages.
  * [Metapost](https://www.tug.org/metapost.html)  ([wikipedia](http://en.wikipedia.org/wiki/MetaPost)).  General purpose graphics engine with a Metafont-based syntax.
  * [Asymptote](http://asymptote.sourceforge.net/), "a powerful descriptive vector graphics language that provides a natural coordinate-based framework for technical drawing."  Syntax based on Metafont.
  * [TikZ/PGF](http://en.wikipedia.org/wiki/PGF/TikZ), a pair very powerful and elegant graphics languages (PGF is low-level, TikZ a high-level language that uses PGF) implemented in TeX(!).  TikZ uses Metafont-like syntax for specifying drawing paths, with considerable enhancement.  The most amazing graphics package going, IMHO.  Poke around in the [examples](http://www.texample.net/tikz/examples/) to see why.
    *  [PGFPlots](http://pgfplots.sourceforge.net/) - "A LaTeX Package to create normal/logarithmic plots in two and three dimensions", based on TikZ/PGF
 
#### Functional languages

  * [Shapes](http://lang-shapes.sourceforge.net/) - "a powerful functional drawing language with LATEX support"
  * 

#### Other vector graphics languages
  * [Postscript](http://en.wikipedia.org/wiki/PostScript) (see also [Ghostscript](http://www.ghostscript.com/), an open source Postscript and PDF interpreter)
  * [SVG](http://en.wikipedia.org/wiki/Scalable_Vector_Graphics) Scaleable Vector Graphics

#### Other:
  * [D3](http://d3js.org/) - data-driven documents, "D3.js is a JavaScript library for manipulating documents based on data. "
  * [Vega](https://github.com/trifacta/vega) "Vega is a visualization grammar, a declarative format for creating, saving and sharing visualization designs."  "With Vega you can describe data visualizations in a JSON format, and generate interactive views using either HTML5 Canvas or SVG."
  * [Processing](http://processing.org/) & [processing.js](http://processingjs.org/)
  * [GLE](http://glx.sourceforge.net/)
  * [JLatexMath](http://forge.scilab.org/index.php/p/jlatexmath/) "JLaTeXMath is a Java library. Its main purpose is to display mathematical formulas written in LaTeX. JLaTeXMath is the best Java library to display LaTeX code."
  * [JEuclid](http://jeuclid.sourceforge.net/) "JEuclid is a complete MathML rendering solution..."
  * [SnuggleTeX](http://www2.ph.ed.ac.uk/snuggletex/documentation/overview-and-features.html) "SnuggleTeX is a free and open-source Java library for converting fragments of LaTeX to XML (usually XHTML + MathML)."

### Graphics Libraries for General Purpose Languages
  * [Matplotlib](http://matplotlib.org/) "a python 2D plotting library which produces publication quality figures"
  * [JFreeChart](http://www.jfree.org/jfreechart/) "a free 100% Java chart library"
  * [Racket Drawing Toolkit](http://docs.racket-lang.org/draw/index.html) is one of several graphics libraries for [Racket](http://racket-lang.org/), a Scheme dialect.

### Data Visualization - languages and software designed specifically for graphical display of data:

  * [Gnuplot](http://www.gnuplot.info/)
  * [R graphics](http://cran.r-project.org/web/views/Graphics.html) (plotting) ([wikibook](http://en.wikibooks.org/wiki/R_Programming/Graphics))
  * [Yorick](http://yorick.sourceforge.net/)
  * [IDL](http://www.exelisvis.com/ProductsServices/IDL.aspx) (free version: [GDL](http://gnudatalanguage.sourceforge.net/))
  * [Tableau](http://www.tableausoftware.com/) (commercial)

### Tools and Utilities

  * [GraphicsMagick](http://www.graphicsmagick.org/) - terrific set of very powerful command line tools - "the swiss army knife of image processing".  GraphicsMagick is a fork of an older project called [ImageMagick](http://www.imagemagick.org/).  They're very similar, but the buzz on the web is that GraphicsMagick is faster.
  * [ESS](http://ess.r-project.org/) "Emacs Speaks Statistics ... an add-on package for emacs text editors such as GNU Emacs and XEmacs. It is designed to support editing of scripts and interaction with various statistical analysis programs such as R, S-Plus, SAS, Stata and JAGS."

### Statistics, Data Visualization

  * [Comparison of statistical packages](http://en.wikipedia.org/wiki/Comparison_of_statistical_packages)
  * [Open source statistical packages](http://en.wikipedia.org/wiki/List_of_statistical_packages#Open_source_statistical_packages)
  * [EDA](http://www.itl.nist.gov/div898/handbook/eda/eda.htm) Exploratory Data Analysis (NIST handbook)
  * [R](http://www.r-project.org/) - see also [R Studio](http://www.rstudio.com/ide/)
  * [Incanter](http://incanter.org/) "is a Clojure-based, R-like platform for statistical computing and graphics."
  * [Gnu PSPP](https://www.gnu.org/software/pspp/) - "GNU PSPP is a program for statistical analysis of sampled data. It is a Free replacement for the proprietary program SPSS, and appears very similar to it with a few exceptions."
  * [SOFA](http://www.sofastatistics.com/home.php) "Statistics Open For All - The user-friendly, open-source statistics, analysis, and reporting package."
  * [Salstat](http://www.salstat.com/) "Rapid statistical analysis of scientific data" Python based [MORIBUND]
  * [Gretl](http://gretl.sourceforge.net/) "Gnu Regression, Econometrics and Time-series Library" a cross-platform software package for econometric analysis
  * [SCaViz](http://jwork.org/scavis/) "an environment for scientific computation, data analysis and data visualization designed for scientists, engineers and students" - Java-based
  * [JAGS](http://mcmc-jags.sourceforge.net/) "Just Another Gibbs Sampler ... a program for analysis of Bayesian hierarchical models using Markov Chain Monte Carlo (MCMC) simulation  not wholly unlike BUGS."

### Math

These systems usually have powerful graphics subsystems with support for drawing plots.

#### Commercial
Magma, Maple, Mathematica and Matlab.

#### Free
  * [Sage](http://www.sagemath.org/) - "a free open-source mathematics software system"
  * [Maxima](http://maxima.sourceforge.net/) - "a computer algebra system"
  * [Mathics](A free, light-weight alternative to Mathematica) - "a free, general-purpose online computer algebra system featuring Mathematica-compatible syntax and functions"
  * [Gnu Octave](http://www.gnu.org/software/octave/)  "a high-level interpreted language, primarily intended for numerical computations. It provides capabilities for the numerical solution of linear and nonlinear problems, and for performing other numerical experiments. It also provides extensive graphics capabilities for data visualization and manipulation...quite similar to Matlab>"
