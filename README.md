ghc-ios-cabal-scripts
=====================

Cabal scripts and package patches for building with ghc-ios.

How to use with cabal-dev
-------------------------

In your source directory execute

    $ path/to/ghc-ios-cabal-scripts/add-all <CABAL-DEV-OPTIONS>

This will download and patch packages and add them via `add-source`. Now install your package (or configure and build) with the following options:

    --hsc2hs-options=--cross-compile

How to add a patch for a package on hackage
-------------------------------------------

    $ unpack <PACKAGE>
    $ cd <PACKAGE-VERSION>
    $ vi ...
    $ git diff > patches/<PACKAGE>
    $ git add patches/<PACKAGE>
    $ git commit

Then send a pull request.
