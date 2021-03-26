# Technical reference for the benchmarks

## Glossary

### <i>b</i>-tagging discriminant

A value assigned to a jet that is correlated with the probability that the jet originated from a [bottom quark](https://en.wikipedia.org/wiki/Bottom_quark). See [<i>b</i>-tagging](https://en.wikipedia.org/wiki/B-tagging).

NanoAOD branch: `Jet_btag`

### Δ<i>R</i>

Equal to sqrt(Δ<i>η</i><sup>2</sup> + Δ<i>φ</i><sup>2</sup>). The most common metric used for distance between four-momenta in hadron colliders.

### <i>η</i>

[Pseudorapidity](https://en.wikipedia.org/wiki/Pseudorapidity), a unitless geometric coordinate used in hadron colliders.

NanoAOD branches: `<object type>_eta`

### Event

A single bunch crossing. Each entry in a NanoAOD `TTree` corresponds to one event. See [Event (particle physics)](https://en.wikipedia.org/wiki/Event_\(particle_physics\)).

### Flavor

A species of elementary particle, including its [antiparticle](https://en.wikipedia.org/wiki/Antiparticle). For example, electrons and positrons are of the same flavor, but muons are another flavor. See [Flavour](https://en.wikipedia.org/wiki/Flavour_\(particle_physics\)).

### Four-momentum

A [four-vector](https://en.wikipedia.org/wiki/Four-vector) with units of momentum. See [Four-momentum](https://en.wikipedia.org/wiki/Four-momentum). Four-momentum in events is often specified by <i>p</i><sub>T</sub>, <i>η</i>, <i>φ</i>, and mass, but addition of four-momenta is only straightforward in the Cartesian coordinates <i>E</i>, <i>p</i><sub>x</sub>, <i>p</i><sub>y</sub>, and <i>p</i><sub>z</sub>. A nice summary of the relationships between these can found [here](https://energyflow.network/docs/utils/).

NanoAOD branches: <i>p</i><sub>T</sub> (in GeV): `<object type>_pt`, <i>η</i>: `<object type>_eta`, <i>φ</i> (in radians): `<object type>_phi`, Mass (in GeV): `<object type>_mass`

### GeV

Gigaelectronvolt, a unit of energy. Also used as shorthand for GeV/<i>c</i> (a unit of momentum) and GeV/<i>c</i><sup>2</sup> (a unit of mass). See [Electronvolt](https://en.wikipedia.org/wiki/Electronvolt). In NanoAOD files, all energies, momenta, and masses are in GeV.

### Invariant mass

Equal to sqrt(<i>E</i><sup>2</sup> - <i>p</i><sup>2</sup>), where <i>E</i> and <i>p</i> are the energy and momentum, respectively, of a given four-momentum. See [Invariant mass](https://en.wikipedia.org/wiki/Invariant_mass).

### Jet

A cone of particles emitted by a collision. A jet is usually represeneted by a four-momentum, which is a sum over the constituent particles. See [Jet (particle physics)](https://en.wikipedia.org/wiki/Jet_\(particle_physics\)).

NanoAOD branches: `Jet_<property>`

### Light lepton

An electron, positron, or muon. See [Lepton](https://en.wikipedia.org/wiki/Lepton). "Light" means less massive than a tau lepton. Neutrinos are also light leptons, but they are generally not detectable in collider experiments. Leptons are represented by their four-momentum and their charge.

NanoAOD branches: Electrons and positrons: `Electron_<property>`, Muons: `Muon_<property>`
(Positrons are considered to be electrons with a positive charge.)

### Missing transverse momentum

The negative vector sum of the transverse momenta of all objects in an event. The magnitude of this vector is written as <i>E</i><sub>T</sub><sup>miss</sup>, also called missing <i>E</i><sub>T</sub> (MET). See [Missing energy](https://en.wikipedia.org/wiki/Missing_energy).

NanoAOD branches: Magnitude (in GeV): `MET_pt`, <i>φ</i> (in radians): `MET_phi`

### NanoAOD

A ROOT-based file format used by the [CMS experiment](https://en.wikipedia.org/wiki/Compact_Muon_Solenoid). It consists of a [TTree](https://root.cern.ch/doc/master/classTTree.html) named `Events` with [TBranches](https://root.cern.ch/doc/master/classTBranch.html) corresponding to the properties of the events.

### <i>φ</i>

[Azimuthal angle](https://en.wikipedia.org/wiki/Spherical_coordinate_system), a spherical coordinate.

NanoAOD branches (in radians): `<object type>_phi`

### ROOT

A [data analysis software framework](https://root.cern.ch/) for high energy physics (HEP). Most HEP data is stored in [ROOT files](https://root.cern.ch/doc/master/classTFile.html), a format produced by the ROOT framework.

### Transverse mass

The transverse mass of a system of missing transverse momentum and a lepton is equal to sqrt(2 * <i>p</i><sub>T, lepton</sub> * <i>E</i><sub>T</sub><sup>miss</sup> * (1 - cos(Δ<i>φ</i>))).

### Transverse momentum

The projection of the momentum onto the <i>xy</i>-plane. The magnitude is usually written as <i>p</i><sub>T</sub>.

NanoAOD branches: Magnitude (in GeV): `<object type>_pt`, <i>φ</i> (in radians): `<object type>_phi`

### Trijet

A group of three jets. The four-momentum of a trijet is the sum of the three jet four-momenta.
