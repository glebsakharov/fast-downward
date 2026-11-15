# `fast-downward-Temporal`

This project leverages the fast-downward DSL to solve temporal planning problems with durationless actions, using the underlying classical planning engine FastDownward. 

This work comprises a Haskell project that interacts with a Python script for computing automata from Linear Temporal Logic formulas and a C++/Python planning engine for solving classical planning problems. Thus there is some interprocess communication involved, requiring FastDownward and the Python script installed locally. 

There is a section on build information: for the Haskell project; the Python script; and the FastDownward planning engine. 

I've demonstrated how to use the output of the Python script to manipulate the DSL into compiling SAS+ files that encode temporal planning problems. This follows the theoretical work by Giuseppe De Giacomo and Moshe Y Vardi, on using classical planning engines to solve temporal planning problems using Deterministic Finite Automata (DFA).

This is no significant attempt at producing a competitive temporal planner, so fast performance times are no thanks to me. This would be down to the work of the researchers and engineers behind the planning DSL and the FastDownward planning engine. I purely wanted to produce a proof of concept, reproducing the work of others.
