## Ab Initio Model
"Ab Initio model" , or "first principle model", where the starting point of the model cannot be further reduced.
If we start from the Schro, to what extend can we reproduce a physical, observable phenomena.

### Formal Systems
Four ingredients: Symbols, Statements(string of symbols: meaningful or meaningless; meaningful: true or false), Derivation rules(convert meaningful statements between each other), Axioms.  
- Symbols: +, =, 1, 2, 3...
- statements: 2+1=3, 1+1=3....
- Derivation rules: add '1' before or after +, and add '1' in the end
- axiom: 1+1=2

Classification of branches of Science 
- Math: search for formal systems with nice properties
- Physics: search for formal system that mimic the behavior of Nature
- Engineering: use the formal system of physics to develop devices

A tree with leaves, trunk, roots on Classical Mechanics:
- roots: axioms, newton's laws
- trunk: derivation rules, calculus
- leaves:statements about observable facts, all mechanical observation

Newtonian mechanics is an ab initio classical mechanics, where we started from the most basic laws. Choice of formal systems is not unique, for example, Langragian Mechanics. Also, not all mechanics are ab initio from newton's law, i.e. friction between surfaces.

### Solid as quantum system
Solid? mine: where constituent particled are bond together with little room for travel or exchange places.

1. A solid is a system of positive nuclei and negative electrons, all electromagnetically interacting with each other, and obeying the equations of motion prescribed by quantum physics. (electrons and nuclei, not atoms)

Properties of a materials = crystal structure + microstructure
microstructure: type/number of defects, grain size, grain orientation.

### Problem Statement
- axioms known, equations soluble
    - classical mechanics, electromagnetism, thermodynamics
    - engineering approach possible
- axioms known, equations cannot to be solved
    - condensed matter physics, material science, chemistry
-  axioms unknown
    - nuclear physics

However, quantum physics are becoming more and more computable. The formal system of Newtonian Mechanics are much more soluble than the formal system of Quantum Mechanics.

## DFT
Many-body Schroginder equations are transformed to SIngle particle Kohn-SHam equations through density functional theory.
What is the catch in the theory? DFT is an exact solution, provided that we know the exchange correlation functional. DFT says it exists, but says nothing about its appearance.

### Functions and Functionals
- Functions: `f: R -> R: x -> f(x)`, maps numbers onto (complex) numbers
- Functionals: `F: ff -> C:f->F[ff]`, maps functions onto (complex) numbers;
![definitions](dft_definitions.png)

### the Schrodinger Equation
Wavefunction is a function
```
\psi: ? -> ?:?->\psi(?)
```
Wavefunctions for electron systems are antisymmetric for particle exchange -- an axiom of quantum physics.
The energy of the solid in Schro can be found -- energy it takes to separate electrons and necleuis to infintie distances from its original ground state.

### Born-Oppenheimer Approximation 
1. exact Hamiltonians
2. Born-Oppenheimer
3. Hartree-Fock or DFT
4. solution techniques
5. Predictions

Born-Oppenheimer approximation, a.k.a. the adiabatic principle. In classical picture, a much more massive object will move so slowly that they are at rest compare to their lighter counterparts, i.e. electrons. It reduces the number of variables.
![Born-Oppenheimer](adiabatic_principle.png)
![Born-Oppenheimer 1](BOA_1.png)
![Born-Oppenheimer 2](BOA_2.png)

### Slater Determinant
Maybe a many body wavefunction is the product of two independent wavefunctions? However, interchanging the two particles would introduce a negative sign.
![slater1](slater_problem.png)

The below incorporates the antisymmetry.
![slater2](slater2.png)

You can rewrite it in determinant form, Slater determinant, and generalize it.
![slater3](slater3.png)
![slater4](slater4.png)

### (post-)Hartree-Fock methods
HF methods search for solutions for Schro. However, we can search only in the subset of all antisymmetric wavefunction. The subset of Slater determinants within the all antisymmetric wavefunctions is then chosen. There is no garuantee our solution would be a Slater determinants. HF methods search for Slater determinants with the lowest energy, and call it the best approximation to the true ground state.

Post-HF methods sample the rest of the antisymmetric functions and try to bridge the gap between HF ground state and the exact ground state solution.

### External Potential - DFT
What to specify in a system:
- Number of electrons
- position and number of nucleui 
The electron-nucleius interaction term (the last in H) gives the energy of N electrons in the electric potential provided by a given set of nuclei at R_A. The aforemention "external potential" determins the type of system you are studying. It is "external" to the electron system.
![external_pot](external_pot.png)

### Electron Density - DFT
Electron density is a function.
![electron_density](electron_density.png)