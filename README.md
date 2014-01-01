# IPython Lambda Notebook

This project is a framework for linguists and especially semanticists developing analyses in compositional semantics.  It aims to provide a means of developing 'digital fragments', following from the method of fragments in Montague grammar.

The project is in an alpha state.  While code is publicly up on github, expect bugs and rapid changes.  Contributions, requests, and suggestions are welcome.  I hope to have a more stable beta by the beginning of summer 2014.

## Installation

Prerequisites: python 3.3.x, and IPython set up to run with python 3.
  * Unfortunately this is not yet easy to install.  
  * For python 3, see [http://www.python.org/](http://www.python.org/).  We do not using OS installed versions, for example, on OS X.
  * The complications lie in getting IPython to work with python 3.
  * For general installation instructions for IPython, see [http://ipython.org/install.html](http://ipython.org/install.html).  A slightly outdated, but more useful document, is at [http://ipython.org/ipython-doc/rel-1.1.0/install/index.html](http://ipython.org/ipython-doc/rel-1.1.0/install/index.html).
  * To run ipython with python 3, you can either install IPythin by using 'python3 setup.py', or run 'python3 ipython.py'
  * Suggestions for improving these instructions are welcome!  The long term goal is to provide the lambda notebook as a standalone app.

## Getting started

Run 'ipython3 notebook' in the main directory of the repository.  Then look through the various notebooks to see examples of what can be done.  I recommend starting (for now) with:
  * LSA Poster examples
  * Lamb demo (old, but thorough for what was available at the time)
  * Composition operations


## Code overview

There are three main parts to the code, structured into meta.py (for metalanguage), types.py, and lang.py.
  * meta.py and types.py together provide a typed logical metalanguage somewhat comparable to nltk.sem.  
  * lang.py provides machinery for doing composition on an object language.

Two additional files, magics.py and parsing.py provide support for using cell magics in the notebook to directly type expressions in the metalanguage.  See the notebooks for demos of what this looks like; better documentation coming soon!  


## NLTK

The file tree_mini.py provides nltk.tree, hacked to work in python 3.  Note that this is _not permanent_, and once nltk supports python 3 directly (in beta now) this will become part of a dependency.  I have also added IPython display routines that will in the future be installed via monkey patching.

See [here](https://github.com/nltk/nltk/blob/develop/LICENSE.txt) for NLTK license information (Apache license).