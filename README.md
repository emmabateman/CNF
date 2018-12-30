# CNF
Converts any context-free grammar into a weakly equivalent grammar in Chomsky Normal Form

# About Chomsky Normal Form
A grammar is in Chomsky Normal Form if all its productions are either of the form:
    A -> BC
or of the form:
    A -> a

Any context-free grammar can be matched to some weakly equivalent grammar in CNF. Weakly equivalent grammars accept/reject the same inputs, but the parses they produce may not have the same structure.

Conversion to Chomsky Normal Form is useful for certain parsing algorithms.

# How to use
The input file should be a context-free grammar in a format supported by NLTK

Example grammar file:
```
# my_grammar.cfg
S -> NP VP
NP -> Det N
VP -> V | V NP
Det -> 'the' | 'a'
N -> 'cat' | 'dog'
V -> 'runs' | 'chases' | 'catches' | 'eats'
```
Example usage:

```
python cnf.py my_grammar.cfg > my_cnf_grammar.cfg
```
# Dependencies
This code requires Python 2.7 and NLTK
