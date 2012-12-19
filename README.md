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

Package build status
--------------------

<pre>
x builds
p builds with patch
? unknown
- won't build

x aeson
x async
x attoparsec
x attoparsec-conduit
x bytestring
x cereal
x cereal-conduit
x conduit
x data-lens
x directory
x explicit-exception
x failure
x filepath
x hashable
- hmatrix
x hosc
x hsc3
- hsc3-lang (hmatrix)
? hsc3-process
? hsc3-server
p lifted-base
x network
x network-conduit
p primitive
x process
x reactive-banana
x resourcet
x split
x system-fileio
x system-filepath
x text
x transformers
x unix
x unordered-containers
x url
p vector
</pre>
