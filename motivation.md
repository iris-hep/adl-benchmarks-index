Functionality motivations for benchmarks
=======================================================

| Benchmark description | Motivation |
|-----------------------|------------|
| Plot the missing <i>E</i><sub>T</sub> of all events. | Loop over events and get an event-level variable. |
| Plot <i>p</i><sub>T</sub> of all jets in all events. | Loop over an array in each event. |
| Plot <i>p</i><sub>T</sub> of jets with \|<i>η</i>\| < 1. | Loop over an array that is filtered. |
| Plot the missing <i>E</i><sub>T</sub> of events that have at least two jets with <i>p</i><sub>T</sub> > 40 GeV. | Loop over an array and aggregate the results to filter at the event level. |
| Plot the missing <i>E</i><sub>T</sub> of events that have an opposite-sign muon pair with an invariant mass between 60 and 120 GeV. | Loop on pairs of objects in one collection and do four-vector algebra. |
| Plot <i>p</i><sub>T</sub> of the trijet system with the mass closest to 172.5 GeV in each event and plot the maximum <i>b</i>-tagging discriminant value among the jets in the triplet. | Loop over combinations of objects in the same collection and extract a property of the combinations other than the key used to sort them. |
| Plot the sum of <i>p</i><sub>T</sub> of jets with <i>p</i><sub>T</sub> > 30 GeV that are not within 0.4 in Δ<i>R</i> of any lepton with <i>p</i><sub>T</sub> > 10 GeV. | Loop over two different collections. |
| For events with at least three leptons and a same-flavor opposite-sign lepton pair, find the same-flavor opposite-sign lepton pair with the mass closest to 91.2 GeV and plot the transverse mass of the missing energy and the leading other lepton. | Perform a task for which the formulation in an imperative language is easy but the translation to a functional query language may be less clear or inefficient. |
