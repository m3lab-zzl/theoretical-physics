Theoretical Physics Reference
-----------------------------

This is an opensource book, available online at:

https://theoretical-physics.com

All files in the repository are licensed under the MIT license. The source code
of the repository is available at:

https://github.com/certik/theoretical-physics

Build
-----

Install prerequisites::

    sudo apt-get install texlive-fonts-recommended texlive-latex-extra texlive-fonts-extra dvipng
    pip install -r requirements.txt

To build the book, do::

    make web

This builds both html and pdf versions, that you can find in the _build
directory.

Build Using Conda
-----------------

Conda build::

    conda env create  -f environment.yml
    # mamba env create -f environment.yml # only if you have mamba installed
    conda activate tprbook
    pip install -r requirements.txt
    make latex
    tectonic _build/latex/theoretical-physics.tex

How to Push to Github
---------------------

First fetch the gh-pages branch and then use this script::

    ./copy-docs

and optionally push the gh-pages branch to github::

    git push github
