Bitcoin 2 integration/staging tree
=====================================

[![Build Status](https://travis-ci.org/bitcoin/bitcoin.svg?branch=master)](https://travis-ci.org/bitcoin/bitcoin)

www.bitc2.org

What is Bitcoin 2?
----------------

Bitcoin 2 is an experimental digital currency that enables instant payments to
anyone, anywhere in the world. Bitcoin 2 uses peer-to-peer technology to operate
with no central authority: managing transactions and issuing money are carried
out collectively by the network. Bitcoin 2 Core is the name of open source
software which enables the use of this currency.

For more information, as well as a binary version of
the Bitcoin 2 Core software, see www.bitc2.org

## Not yet ready for release

A lot of the source code for Bitcoin 2 is not yet ready for release and not all of the files required to build the software are yet in Github. It will all be available as soon as Bitcoin 2 Core wallets are released, on the day that the Bitcoin 2 network goes live.

License
-------

Bitcoin 2 is released under the terms of the MIT license. See [COPYING](COPYING) for more
information or see https://opensource.org/licenses/MIT.





Development Process
-------------------

The `master` branch is regularly built and tested, but is not guaranteed to be
completely stable. [Tags](https://github.com/bitcoin/bitcoin/tags) are created
regularly to indicate new official, stable release versions of Bitcoin Core.

The contribution workflow is described in [CONTRIBUTING.md](CONTRIBUTING.md).

The developer [mailing list](https://lists.linuxfoundation.org/mailman/listinfo/bitcoin-dev)
should be used to discuss complicated or controversial changes before working
on a patch set.

Developer IRC can be found on Freenode at #bitcoin-core-dev.

Testing
-------

Testing and code review is the bottleneck for development; we get more pull
requests than we can review and test on short notice. Please be patient and help out by testing
other people's pull requests, and remember this is a security-critical project where any mistake might cost people
lots of money.

### Automated Testing

Developers are strongly encouraged to write [unit tests](src/test/README.md) for new code, and to
submit new unit tests for old code. Unit tests can be compiled and run
(assuming they weren't disabled in configure) with: `make check`. Further details on running
and extending unit tests can be found in [/src/test/README.md](/src/test/README.md).

There are also [regression and integration tests](/test), written
in Python, that are run automatically on the build server.
These tests can be run (if the [test dependencies](/test) are installed) with: `test/functional/test_runner.py`

The Travis CI system makes sure that every pull request is built for Windows, Linux, and OS X, and that unit/sanity tests are run automatically.

### Manual Quality Assurance (QA) Testing

Changes should be tested by somebody other than the developer who wrote the
code. This is especially important for large or high-risk changes. It is useful
to add a test plan to the pull request description if testing the changes is
not straightforward.
