# `fast-downward-Temporal`

# Temporal Planning with the Fast Downward Haskell DSL

This project extends the Fast Downward Haskell DSL to support temporal planning problems with instantaneous actions, using the underlying classical planning engine, Fast Downward.

The implementation combines three components:

- **Haskell:** An extension to the existing embedded planning DSL, incorporating temporal constraints into the planning problem representation.
- **Python:** A script using the `flloat` library to translate Linear Temporal Logic (LTL) formulas into Deterministic Finite Automata (DFA).
- **Fast Downward:** The underlying classical planning engine, which searches for plans satisfying the resulting planning problem.

The components communicate through interprocess communication. Consequently, building and running the project requires a local installation of Fast Downward and the necessary Python dependencies.

This repository includes build instructions for the Haskell project, the Python script and the Fast Downward planning engine.

The central idea is to use the DFA generated from an LTL formula to extend the planning problem with automaton state and transition information. This allows temporal constraints to be encoded into SAS+ planning problems and solved using an existing classical planning engine. The approach follows established theoretical work by Giuseppe De Giacomo and Moshe Y. Vardi on the use of automata in temporal planning.

**Scope and motivation**

This project is intended as a proof of concept demonstrating how temporal planning can be integrated into an existing functional embedded domain-specific language. It is not an attempt to develop a new temporal planning algorithm or a competitive temporal planner.

The underlying planning performance is primarily attributable to the existing DSL and Fast Downward. The contribution of this project is the integration of temporal logic and automata-based reasoning into that existing framework, while leaving the underlying classical planning engine unchanged.
