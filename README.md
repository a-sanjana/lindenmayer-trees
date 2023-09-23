# Lindenmayer Trees
## Algorithm Descrition
Lindenmayer systems or L-systems use parallel rewriting systems to model various organisms and fractals. It consists of an alphabet to make strings, an axiom and set of rules for production. L-Systems are recursive in nature, which leads to self-similarity. Our project consists of two main shapes - line and circle. The line drawing is an implementation of Bressenham's Line Algorithms, and the cicle utilizes the Midpoint Circle Algorithm. To draw the final output, we use the concept of L-Systems. The generated string is parsed and the set of production rules are applied. These rules are described above. The outputs produced with increasing iterations is shown above as well.
## Symbols
- F : indicates to draws a line at a given coordinate at the specified angle and length.
- \- : rotate right
- \+ : rotate left
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
- Axiom : [X]++[X]++[X]++[X]++[X]
- Rules
    - W=YF++ZF-—XF[-YF-—WF]++
    - X=C0+YF–ZF[C1—WF–XF]+
    - Y=-WF++XF[+++YF++ZF]-
    - Z=–YF++++WF[+ZF++++XF]–XF
    - F=
- Iterations: 4
## Output Images
### Iteration 1
![](/Output%20images/it1.png)
### Iteration 2
![](/Output%20images/it2.png)
### Iteration 3
![](/Output%20images/it3.png)
### Iteration 4
![](/Output%20images/it4.png)
### Iteration 5 : Final Output
![](/Output%20images/final_image.png)
## Timing Analysis
With each iteration, the time for execution(in milliseconds) increases drastically.
![](/Output%20images/TimeAnalysis.png)
## Aditional Notes
This project is pat of the course 'Computer Graphics'. To access the HTML documentation, please refer to the [index.html](/Documentation/html/index.html) file.
## References
[1](https://paulbourke.net/fractals/lsys/)
[2](https://www.youtube.com/watch?v=f6ra024-ASY&t=1134s)
[3](http://alvyray.com/Papers/CG/PlantsFractalsandFormalLanguages.pdf)
[4](https://docs.racket-lang.org/lindenmayer/Interpreting_L-systems.html?source=post_page--&mdash;98e07de6bd63-------------------&mdash;)
