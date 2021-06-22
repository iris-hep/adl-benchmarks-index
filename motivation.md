Functionality motivations for benchmarks
=======================================================

| Benchmark description | Motivation |
|-----------------------|------------|
| Plot the <i>E</i><sub>T</sub><sup>miss</sup> of all events. | Loop over events and get an event-level variable. |
| Plot the <i>p</i><sub>T</sub> of all jets. | Loop over an array in each event. |
| Plot the <i>p</i><sub>T</sub> of jets with \|<i>η</i>\| < 1. | Loop over an array that is filtered. |
| Plot the <i>E</i><sub>T</sub><sup>miss</sup> of events that have at least two jets with <i>p</i><sub>T</sub> > 40 GeV. | Loop over an array and aggregate the results to filter at the event level. |
| Plot the <i>E</i><sub>T</sub><sup>miss</sup> of events that have an opposite-charge muon pair with an invariant mass between 60 and 120 GeV. | Loop on pairs of objects in one collection and do four-vector algebra. |
| For events with at least three jets, plot the <i>p</i><sub>T</sub> of the trijet four-momentum that has the invariant mass closest to 172.5 GeV in each event and plot the maximum <i>b</i>-tagging discriminant value among the jets in this trijet. | Loop over combinations of objects in the same collection and extract a property of the combinations other than the key used to sort them. |
| Plot the scalar sum in each event of the <i>p</i><sub>T</sub> of jets with <i>p</i><sub>T</sub> > 30 GeV that are not within 0.4 in Δ<i>R</i> of any light lepton with <i>p</i><sub>T</sub> > 10 GeV. | Loop over two different collections. |
| For events with at least three light leptons and a same-flavor opposite-charge light lepton pair, find such a pair that has the invariant mass closest to 91.2 GeV in each event and plot the transverse mass of the system consisting of the missing tranverse momentum and the highest-<i>p</i><sub>T</sub> light lepton not in this pair. | Perform a task for which the formulation in an imperative language is easy but the translation to a functional query language may be less clear or inefficient. |
