# Introduction #

Wikisrvd, the core component of wiki2touch, is a mini web server with the capability to decompress, parse the MediaWiki XML dump and rewrite into an HTML.

Besides running on a jailbroken iPhone/iPad/iPod touch, wikisrvd could also be useful as a mini server hosting read-only images of MediaWiki sites on various OSes.

# Details #

Building the wikisrvd requires:

  * Clang/LLVM, or GCC with c++ support. (It has been tested to work with Clang 3.0 and g++ 4.6 on Ubuntu 12.04 x86\_64)
  * CMake and GNU Make Utility
  * Header files and libraries for libbz2 and libcrypto.

First, check-out source code from branches:
```
  svn co https://wiki2touch-standalone-ui.googlecode.com/svn/branches/wikisrvd wikisrvd
```
Then, run CMake to generate the Makefile:
```
  cd wikisrvd/
  cmake .
```
Build:
```
  make
```
As the building finished, an executable `wikisrvd' would be generated. Copy it into `daemon' directory:
```
  cp wikisrvd ./daemon/
```
To run the daemon:
```
  ./daemon/wikisrvd
```