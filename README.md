Levelcoin integration/staging tree
================================

http://www.swisopensource.com

Copyright (c) 2009-2014 Bitcoin Developers
Copyright (c) 2011-2014 Litecoin Developers
Copyright (c) 2015-2017 Levelcoin Developers

Important News
-----------------
We have fixed BlockChain fork Issue and Updated Protocol Version from 70002 to 71003. 
Difficulty algorithm changed to DGW.. 
Changes take effect on Jan 25, 00:00:00 GMT.

What is Levelcoin?
----------------

Levelcoin is a lite version of Bitcoin using scrypt as a proof-of-work algorithm.
 - 60 minutes block targets
 - subsidy halves in 840k blocks (~4 years)
 - ~3.1 billion total coins

 - 12 coins per block
 - 10 blocks to retarget difficulty

For more information, as well as an immediately useable, binary version of
the Levelcoin client sofware, see http://www.swisopensource.com

License
-------

Levelcoin is released under the terms of the MIT license. See `COPYING` for more
information or see http://opensource.org/licenses/MIT.

Development process
-------------------

Developers work in their own trees, then submit pull requests when they think
their feature or bug fix is ready.

If it is a simple/trivial/non-controversial change, then one of the Levelcoin
development team members simply pulls it.

If it is a *more complicated or potentially controversial* change, then the patch
submitter will be asked to start a discussion with the devs and community.

The patch will be accepted if there is broad consensus that it is a good thing.
Developers should expect to rework and resubmit patches if the code doesn't
match the project's coding conventions (see `doc/coding.txt`) or are
controversial.


Testing
-------

Testing and code review is the bottleneck for development; we get more pull
requests than we can review and test. Please be patient and help out, and
remember this is a security-critical project where any mistake might cost people
lots of money.

### Automated Testing

Developers are strongly encouraged to write unit tests for new code, and to
submit new unit tests for old code.

Unit tests for the core code are in `src/test/`. To compile and run them:

    cd src; make -f makefile.unix test

Unit tests for the GUI code are in `src/qt/test/`. To compile and run them:

    qmake BITCOIN_QT_TEST=1 -o Makefile.test bitcoin-qt.pro
    make -f Makefile.test
    ./levelcoin-qt_test

