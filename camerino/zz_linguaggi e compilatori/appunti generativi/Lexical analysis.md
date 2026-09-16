## Lexical Analysis

### Key Concepts

- **Tokens**: Pairs consisting of a token name and optional attribute value
- **Patterns**: Descriptions of the form lexemes may take
- **Lexemes**: Sequences of characters matching a token's pattern

### Role of Lexical Analyzer (Lexer)

- Classify program substrings according to token class
- Communicate tokens to parser
- The goal is to partition the string. This is implemented by reading left-to-right, recognising one token at a time.
- “Lookahead” may be required to decide where one token ends and the next token begins
	_DECLARE(ARG1,...,ARGN) 
  Is DECLARE a keyword or an array reference? Need for an unbounded lookahead_

## Lexical Analysis: How can we do it?
We need to define which is the set of strings in any token class. Therefore we need to choose the right mechanisms to describe such sets: 
- Reducing at minimum the complexity needed to recognise lexemes 
- Identifying effective and simple ways to describe the patterns
### Regular Expressions (RegEx)

- Used to specify patterns for tokens
- Syntax includes concatenation, union, Kleene star, etc.
- Semantics defined by meaning function L

### Finite Automata

- Used to recognize tokens specified by RegEx
- Two types:
    - Deterministic Finite Automata (DFA)
    - Nondeterministic Finite Automata (NFA)

### Key Algorithms

1. Thompson's Construction: RegEx → NFA
2. Subset Construction: NFA → DFA
3. DFA Minimization

### Lexical Analyzer Implementation

- Combine NFAs for all token patterns
- Use ε-transitions to connect to a new start state
- Implement matching rules:
    - Longest match rule
    - First listed rule for conflicts

### Optimization

- Convert combined NFA to DFA
- Minimize DFA states
- Retain information on final states for correct token identification

### Formal Language Theory

- Chomsky hierarchy of grammars and languages
- Regular languages recognized by finite automata
- Context-free languages recognized by pushdown automata

### Key Takeaways

- Lexical analysis is the first phase of compilation
- Regular expressions and finite automata are fundamental tools
- Optimization techniques like DFA minimization improve efficiency
- Understanding of formal language theory underlies lexical analysis