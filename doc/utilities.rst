.. sectionauthor:: Dan Blanchard <dblanchard@ets.org>

Utilitiy Scripts
================
In addition to the main script, :doc:`run_experiment <run_experiment>`, SKLL
comes with a number of helpful utility scripts that can be used to prepare
feature files and perform other routine tasks. Each is described briefly below.
For full details of how to use each of these scripts, just run them with the
``--help`` option.

arff_to_megam
-------------
Takes an ARFF file and outputs a MegaM-compatible file to be run with the
``-fvals`` switch. Assumes last field is class. Ignores any relational, string,
or date fields. Automatically converts nominals to numerals.

csv_to_megam
-------------
Takes a delimited file with a header line and converts it to MegaM ``-fvals``
format.

filter_megam
------------
Filter MegaM file to remove features with names in stop word list (or non
alphabetic characters). Also has side-effect of removing ``TEST``, ``TRAIN``,
and ``DEV`` lines if they are present.

generate_predictions
--------------------
Loads a trained model and outputs predictions based on input feature files.
Useful if you want to reuse a trained model as part of a larger system without
creating configuration files.

join_megam
----------
Combine MegaM files that contain features for the same examples.

megam_to_arff
-------------
Takes a MegaM-compatible file to be run with the ``-fvals`` switch and outputs
a Weka-compatible ARFF file to STDOUT.

megam_to_libsvm
---------------
Takes a MegaM-compatible file to be run with the ``-fvals`` switch and outputs a
LibSVM/LibLinear-compatible file to STDOUT.

print_model_weights
-------------------
Prints out the weights of a given trained model.