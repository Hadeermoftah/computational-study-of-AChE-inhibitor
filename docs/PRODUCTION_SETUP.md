# Production MD Setup

- GROMACS version: 2023.3
- Integrator: leap-frog MD
- Time step: 0.002 ps (2 fs)
- Number of steps: 10,000,000
- Total production time: 20 ns
- Continuation from NPT: yes

## Constraints
- Algorithm: LINCS
- Constrained bonds: hydrogen bonds
- LINCS iterations: 1
- LINCS order: 4

## Nonbonded interactions
- Cutoff scheme: Verlet
- Neighbor-list update: every 80 steps
- rlist: 1.2 nm
- van der Waals: force-switch
- rvdw-switch: 1.0 nm
- rvdw: 1.2 nm
- Electrostatics: PME
- rcoulomb: 1.2 nm
- PME order: 4
- Fourier spacing: 0.16 nm

## Temperature coupling
- Thermostat: V-rescale
- Groups: Protein_6F, Water_and_ions
- tau_t: 0.1 ps
- Reference temperature: 300 K

## Pressure coupling
- Barostat: Parrinello-Rahman
- Coupling type: isotropic
- tau_p: 2.0 ps
- Reference pressure: 1.0 bar
- Compressibility: 4.5e-5 bar^-1

## Output
- Energies: every 10 ps
- Log: every 10 ps
- Compressed coordinates: every 10 ps
