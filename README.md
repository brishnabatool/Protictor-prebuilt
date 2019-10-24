# Protictor
An automatic corrector or PROMELA models

Usage: ./protictor <filename>.pml [-vN]
  
Performs corrections iteratively on the model <filename>.pml, attacking one error at a time.

For each correction performed, Protictor produces a new updated model, named <filename>\_<versionNumber>.pml
The last file in this sequence is the complete, corrected model.
Protictor also stores the SPIN trail produced at each step, named <filename>\_<versionNumber>.pml.trail. (This file is relevant only for users familiar with SPIN, and is included as an interesting addition for them to play around with.)


Note:
In the PROMELA file, each statement must be on a separate line
There must be no active processes (init must run all starting proceses)
This version does not support inline and #define.
  
  
The version of SPIN included in this package is a customized one, with a few bugs fixed and a few changes made to accomodate tool-to-tool interfacing with Protictor.