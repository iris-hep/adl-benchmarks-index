[![DOI](https://zenodo.org/badge/188481137.svg)](https://zenodo.org/badge/latestdoi/188481137)

Introduction
============

This repository is intended to maintain a list of common agreed-upon benchmark analysis tasks that can be used to exemplify, test, and compare different languages and approaches used for analysis. Also listed here are public data files available to run these benchmarks on and the repositories of actual implementations of these benchmarks.

Functionality benchmarks
========================

1. Plot the <i>E</i><sub>T</sub><sup>miss</sup> of all events.
1. Plot the <i>p</i><sub>T</sub> of all jets.
1. Plot the <i>p</i><sub>T</sub> of jets with |<i>η</i>| < 1.
1. Plot the <i>E</i><sub>T</sub><sup>miss</sup> of events that have at least two jets with <i>p</i><sub>T</sub> > 40 GeV.
1. Plot the <i>E</i><sub>T</sub><sup>miss</sup> of events that have an opposite-charge muon pair with an invariant mass between 60 and 120 GeV.
1. For events with at least three jets, plot the <i>p</i><sub>T</sub> of the trijet four-momentum that has the invariant mass closest to 172.5 GeV in each event and plot the maximum <i>b</i>-tagging discriminant value among the jets in this trijet.
1. Plot the scalar sum in each event of the <i>p</i><sub>T</sub> of jets with <i>p</i><sub>T</sub> > 30 GeV that are not within 0.4 in Δ<i>R</i> of any light lepton with <i>p</i><sub>T</sub> > 10 GeV.
1. For events with at least three light leptons and a same-flavor opposite-charge light lepton pair, find such a pair that has the invariant mass closest to 91.2 GeV in each event and plot the transverse mass of the system consisting of the missing tranverse momentum and the highest-<i>p</i><sub>T</sub> light lepton not in this pair.

For the motivations behind these benchmarks, see [motivation.md](motivation.md). For a technical reference of the terms used in the benchmarks, see [reference.md](reference.md).

Input data files
================

* [Converted to NanoAOD](https://github.com/cms-opendata-analyses/AOD2NanoAODOutreachTool) from [2012 CMS open data](http://opendata.cern.ch/record/6021):
  * root://eospublic.cern.ch//eos/root-eos/benchmark/Run2012B_SingleMu.root (16 GiB, 53 million events)

Language implementations
========================

|Repository|Language|Description|
|----------|--------|-----------|
|[opendata-benchmarks](https://github.com/root-project/opendata-benchmarks)|RDataFrame|RDataFrame is a componenent of [ROOT](https://root.cern/) that provides a high-level interface for analyzing [TTrees](https://root.cern.ch/doc/master/classTTree.html) and other data formats. Each task is solved with a simpler syntax useful in interpreted ROOT macros as well as a fully compiled C++ syntax for best performance. |
|[nail](https://github.com/arizzi/nail/tree/master/benchmarks)|NAIL (Natual Analysis Implementation Language)||
|[groot](https://github.com/go-hep/examples/tree/master/groot/bench-opendata)|[Go](https://golang.org)|Part of the [Go-HEP](https://go-hep.org/) project, `groot` is a pure Go package that provides read/write access to ROOT files|
|[coffea](https://github.com/CoffeaTeam/coffea-benchmarks/tree/master)|Python + Numpy|[Coffea](https://github.com/CoffeaTeam/coffea) builds on numpy and awkward-array for columnar data analysis in Python|
|[bamboo](https://github.com/pieterdavid/bamboo-adl-benchmarks)|Python + RDataFrame|The [bamboo](https://gitlab.cern.ch/cp3-cms/bamboo) analysis framework provides a high-level Python interface to RDataFrame (technically an embedded domain-specific language)|
|[ana](https://github.com/pieterdavid/ana-benchmarks)| C++ | [ana](https://github.com/taehyounpark/ana) is a columnar data analysis interface, with support for arbitrary dataset formats, columnar data types, and results output through user-side implementations. |
|[Rumble](https://github.com/RumbleDB/hep-iris-benchmark-jsoniq)|[JSONiq](https://www.jsoniq.org/) (an [XQuery](https://en.wikipedia.org/wiki/XQuery) dialect for [JSON](https://en.wikipedia.org/wiki/JSON) data)|Most data in ROOT files can be exposed in the JSON data model and can thus be processed by JSONiq. This implementation is targeted to be run on [Rumble](https://rumbledb.org/), a JSONiq implementation on top of Spark, but could be run by any other JSONiq processor.|
|[BigQuery](https://github.com/RumbleDB/iris-hep-benchmark-bigquery)|[BigQuery's dialect](https://cloud.google.com/bigquery/docs/reference/standard-sql/query-syntax) of [SQL](https://en.wikipedia.org/wiki/SQL)|SQL is arguably the most wide-spread language for querying structured data. Since SQL:1999, it supports arrays and structured types and is thus, in principle, suited for typical HEP analyses, though not many implementations support these features. BigQuery's dialect is based on SQL:2011, supports the mentioned features, and has a few additional language constructs that make queries more concise.|
|[PrestoDB](https://github.com/RumbleDB/iris-hep-benchmark-presto)|[PrestoDB's dialect](https://prestodb.io/docs/current/sql/select.html) of [SQL](https://en.wikipedia.org/wiki/SQL) |Like BigQuery, Presto has some support for arrays and structured types; however, it only has limited support for nested queries and a more verbose syntax than BigQuery.|
|[Amazon Athena](https://github.com/RumbleDB/iris-hep-benchmark-athena)|[Athena's dialect](https://docs.aws.amazon.com/athena/latest/ug/ddl-sql-reference.html) of [SQL](https://en.wikipedia.org/wiki/SQL)|Athena is a fully-managed Query-as-a-Service system based on PrestoDB with attractive scalability and pricing but a few more limitations than Presto (most importantly, no support for user-defined functions).|
|[SQL++ (AsterixDB)](https://github.com/RumbleDB/iris-hep-benchmark-sqlpp)|[SQL++](https://asterixdb.apache.org/docs/0.9.6/sqlpp/manual.html)|[AsterixDB](https://asterixdb.apache.org/) is a Big Data platform specialized for semi-structured data. Its query language is thus designed to deal with nested data intuitively.|
|[UnROOT.jl](https://github.com/Moelf/ADLBenchmark.jl)|[Julia](https://julialang.org/)|Pure Julia implementation utilizing packages developed by [JuliaHEP](https://github.com/JuliaHEP/) as a demonstration of ease of use, flexibility, and peak performance at the same time for end-user analysis.|

Adding new benchmarks, data, or implementations
===============================================

* Additional benchmarks or public data files can be suggested as GitHub issues on this project to start a discussion within the [HSF Data Analysis Working Group](https://hepsoftwarefoundation.org/workinggroups/dataanalysis.html) community.
* Suggested modifications to the layout of this repository are also welcome as new GitHub issues.
* If you would like to add a repository with a new implementation of the benchmarks, go ahead and submit a pull request with the proposed changes.
