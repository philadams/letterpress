letterpress
===========

Given a nicely written document in pandoc markdown, output a pretty HTML
document. Complete with bibtex-based references and a mobile-first stylesheet.

To create `./gen` with all the necessary html and css files, ready for upload:

`make SRC=dissertation html`

![Sample HTML output](./sample-out.png)

Uses pandoc, normalize.css, bootstrap 3.x, and make. CSL sheets are available at
https://github.com/citation-style-language/styles.

installation
------------

This project depends on bower (a node package) and pandoc (a Haskell package).
Build happens with `make`.  If you want PDF generation, you'll also need a TeX
library. If you've got these already, then simply run

    git clone https://github.com/philadams/letterpress.git
    pip install -r requirements.txt
    bower install


installing all the dependencies
-------------------------------

If you'd like PDF generation, install TeX using MacTeX
(http://www.tug.org/mactex). You'll really only need the small BasicTeX
library.

Then we'll need pandoc:

    brew install haskell-platform
    cabal install pandoc

And bower:

    brew install node
    npm install -g bower

And then follow the short installation instructions above.

Please note: if you get stuck installing things on Ubuntu, it's probably a
packaging error. A common issue surrounds the packaging of pandoc on Ubuntu and
installing pandoc from apt instead of using Haskell's cabal. You can fix it by
following directions at http://johnmacfarlane.net/pandoc/faqs.html.

future
------

- consider moving references to csl/json format (removing need for bibtex)
