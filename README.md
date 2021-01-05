Introduction
============
This repository is intended to maintain a list of common agreed-upon benchmark analysis tasks that can be used to exemplify, test, and compare different languages and approaches used for analysis. Also listed here are public data files available to run these benchmarks on and the repositories of actual implementations of these benchmarks.

Functionality benchmarks
========================

1. Plot the missing <i>E</i><sub>T</sub> of all events.
1. Plot <i>p</i><sub>T</sub> of all jets in all events.
1. Plot <i>p</i><sub>T</sub> of jets with |<i>η</i>| < 1.
1. Plot the missing <i>E</i><sub>T</sub> of events that have at least two jets with <i>p</i><sub>T</sub> > 40 GeV.
1. Plot the missing <i>E</i><sub>T</sub> of events that have an opposite-sign muon pair with an invariant mass between 60 and 120 GeV.
1. Plot <i>p</i><sub>T</sub> of the trijet system with the mass closest to 172.5 GeV in each event and plot the maximum <i>b</i>-tagging discriminant value among the jets in the triplet.
1. Plot the sum of <i>p</i><sub>T</sub> of jets with <i>p</i><sub>T</sub> > 30 GeV that are not within 0.4 in Δ<i>R</i> of any lepton with <i>p</i><sub>T</sub> > 10 GeV.
1. For events with at least three leptons and a same-flavor opposite-sign lepton pair, find the same-flavor opposite-sign lepton pair with the mass closest to 91.2 GeV and plot the transverse mass of the missing energy and the leading other lepton.

For more details and the motivations behind these benchmarks, see [here](benchmark-motivations.md).

Input data files
================

* Converted from 2012 CMS open data (17 GB, 54 million events):
  * root://eospublic.cern.ch//eos/root-eos/benchmark/Run2012B_SingleMu.root

Language implementations
========================

|Repository|Language|Description|
|----------|--------|-----------|
|[opendata-benchmarks](https://github.com/stwunsch/opendata-benchmarks)|RDataFrame||
|[nail](https://github.com/arizzi/nail/tree/master/benchmarks)|NAIL (Natual Analysis Implementation Language)||
|[groot](https://github.com/go-hep/examples/tree/master/groot/bench-opendata)|[Go](https://golang.org)|Part of the [Go-HEP](https://go-hep.org/) project, `groot` is a pure Go package that provides read/write access to ROOT files|
|[coffea](https://github.com/mat-adamec/coffea-benchmarks)|Python + Numpy|[Coffea](https://github.com/CoffeaTeam/coffea) builds on numpy and awkward-array for columnar data analysis in Python|
|[bamboo](https://github.com/pieterdavid/bamboo-adl-benchmarks)|Python + RDataFrame|The [bamboo](https://gitlab.cern.ch/cp3-cms/bamboo) analysis framework provides a high-level Python interface to RDataFrame (technically an embedded domain-specific language)|
|[rumble](https://github.com/RumbleDB/hep-iris-benchmark-jsoniq)|[JSONiq](https://www.jsoniq.org/) (an [XQuery](https://en.wikipedia.org/wiki/XQuery) dialect for [JSON](https://en.wikipedia.org/wiki/JSON) data)|Most data in ROOT files can be exposed in the JSON data model and can thus be processed by JSONiq. This implementation is targeted to be run on [Rumble](https://rumbledb.org/), a JSONiq implementation on top of Spark, but could be run by any other JSONiq processor.|

Adding new benchmarks, data, or implementations
===============================================

* Additional benchmarks or public data files can be suggested as GitHub issues on this project to start a discussion within the [HSF Data Analysis Working Group](https://hepsoftwarefoundation.org/workinggroups/dataanalysis.html) community.
* Suggested modifications to the layout of this repository are also welcome as new GitHub issues.
* If you would like to add a repository with a new implementation of the benchmarks, go ahead and submit a pull request with the proposed changes.
