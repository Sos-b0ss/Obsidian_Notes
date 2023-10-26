Sources:
https://gitlab.com/pdftk-java/pdftk
\
This is a port of [pdftk](https://www.pdflabs.com/tools/pdftk-server/) into Java.
\
The current goals are to keep functionality as compatible with the original as it is reasonable, to fix any issues present in the original (correctness takes precedence over compatibility, see the [differences](#known-differences-with-pdftk)), and to clean up the code. New functionality may be added, but it is not a priority.
\
So far all code has been manually translated and it passes the test suite of [php-pdftk](https://github.com/mikehaertl/php-pdftk), but [more testing is needed](https://pdftk-java.gitlab.io/pdftk/coverage/). Due to the differences between C++ and Java, it is likely that a few bugs have sneaked in with respect to the original; any help in catching them will be appreciated.
