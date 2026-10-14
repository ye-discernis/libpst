# readpst regression tests.
#
# They need a real PST file, and none is shipped. Point LIBPST_TEST_PST at a
# .pst file or a directory of .pst files; without it the tests are skipped:
#
#   make check LIBPST_TEST_PST=/path/to/mail.pst
#
# See the comment at the top of each test for what it checks, and how to run
# it against an AddressSanitizer build.

TESTS = readpst-embedded-rfc822.sh
EXTRA_DIST = $(TESTS) valgrind.supp
AM_TESTS_ENVIRONMENT = \
    READPST='$(abs_top_builddir)/src/readpst'; export READPST; \
    LIBTOOL='$(LIBTOOL)'; export LIBTOOL; \
    VALGRIND_SUPP='$(abs_srcdir)/valgrind.supp'; export VALGRIND_SUPP;
