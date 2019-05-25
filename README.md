Introduction
============
This repository is intended to maintain a list of common agreed-upon benchmark analysis tasks that can be used to exemplify, test, and compare different languages and approaches used for analysis. Also listed here are public data files available to run these benchmarks on and the repositories of actual implementations of these benchmarks.

Functionality benchmarks
========================

1. Plot the missing <i>E</i><sub>T</sub> of all events
1. Plot <i>p</i><sub>T</sub> of all jets in all events
1. Plot <i>p</i><sub>T</sub> of jets with <i>p</i><sub>T</sub> > 20 GeV and |<i>η</i>| < 1
1. Plot the missing <i>E</i><sub>T</sub> of events that have at least two jets with <i>p</i><sub>T</sub> > 40 GeV
1. Plot the missing <i>E</i><sub>T</sub> of events that have an opposite-sign muon pair with an invariant mass between 60 and 120 GeV
1. Plot <i>p</i><sub>T</sub> of the tri-jet system with mass closest to 172.5 GeV, and plot the maximum <i>b</i>-tagging discriminant value among the jets in the triplet
1. Plot the sum of <i>p</i><sub>T</sub> of jets with <i>p</i><sub>T</sub> > 30 GeV that are not within ΔR 0.4 of a lepton with <i>p</i><sub>T</sub> > 10 GeV
1. For events with at least three leptons and a same-flavor opposite-sign lepton pair, find the same-flavour opposite-sign lepton pair with mass closest to 91.2 GeV and plot the transverse mass of the missing energy and the leading other lepton

Input data files
================

* Converted from 2012 CMS open data (17 GB, 54 million events): root://eospublic.cern.ch//eos/root-eos/benchmark/Run2012B_SingleMu.root

Language implementations
========================

* [LINQtoROOT, TTreeReader, RDataFrame, and uproot](https://github.com/gordonwatts/analysis-plot-comparison)
* [RDataFrame](https://github.com/stwunsch/opendata-benchmarks)
* [NAIL (Natual Analysis Implementation Language)](https://github.com/arizzi/nail/tree/master/benchmarks)

Adding new benchmarks, data, or implementations
===============================================

Additions to any of the above lists (new benchmarks/challenges, public data files, or implementation repositories) can be suggested by creating a GitHub issue in this project.
