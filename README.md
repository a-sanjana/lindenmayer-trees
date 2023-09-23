# Lindenmayer Trees
## Symbols
- F : indicates to draws a line at a given coordinate at the specified angle and length.
- - : rotate right
- + : rotate left
- [ : save current state
- ] : restore previous state
- / : draw circle at the end of the line
- C0: change drawing colour to the first colour in the matrix
- C1: change drawing colour to the second colour in the matrix
- C2: change drawing colour to the second colour in the matrix
## Axioms and Rules
### Tree
- Axiom : F
- Rule : F = C0FC1/F+[+F-F-C2/F]-[-C0F+F+F]
- Iterations: 5
### Sun
-Axiom : [X]++[X]++[X]++[X]++[X]
-Rules
    - W=YF++ZF-—XF[-YF-—WF]++
    - X=C0+YF–ZF[C1—WF–XF]+
    - Y=-WF++XF[+++YF++ZF]-
    - Z=–YF++++WF[+ZF++++XF]–XF
    - F=
-Iterations: 4
## Output Images
### Iteration 1

### Iteration 2
### Iteration 3
### Iteration 4
### Iteration 5 : Final Output