Download Link: https://assignmentchef.com/product/solved-csc336s-assignment-1
<br>
Please write your family and given names and <strong>underline </strong>your family name on the front page of your paper.

All questions <strong>must </strong>be written in latex, and compiled to a single pdf. All code and output of Q1 and Q3 should be <em>embedded </em>into latex. Code and output should be embedded with <em>fixed-width fonts</em>, e.g. Courier. Font size of all fonts must be 12.

What to submit:

<ul>

 <li>The single pdf file a1.pdf (with embedded code and output).</li>

 <li>The latex source file of A1.</li>

 <li>Any source code you wrote (for computation, etc).</li>

</ul>

Thus, the code will be available within latex/pdf, <em>as well as </em>separately.

<strong>1.</strong>

<ul>

 <li>[<em>10 points</em>] Find the condition number of <em>f </em>(<em>x</em>) = (<em>a </em>+ <em>x</em>)<sup>1/4 </sup>− <em>a</em><sup>1/4</sup>, for <em>x </em>&gt; 0, <em>a </em>&gt; 0 and study whether there are ranges of <em>x</em>∈IR<sup>+ </sup>for which the computation of <em>f </em>is ill-conditioned. (You may need to use de l’ Hospital’s rule.)</li>

 <li>[<em>10 points</em>] Consider the (numerical) stability of the computation of the expression (<em>a </em>+ <em>x</em>)<sup>1/4 </sup>− <em>a</em><sup>1/4</sup>, for <em>x </em>&gt; 0, <em>a </em>&gt; 0, when <em>x </em>is close to 0. Explain what problems the computation of the expression may give rise to. Propose a mathematically equivalent expression that is likely to be more stable for <em>x </em>close to 0, and explain.</li>

 <li>[<em>10 points</em>] Set <em>a </em>=     Write     a             MATLAB or equivalent script that goes through the values of             <em>x             </em>in</li>

</ul>

{10<sup>−20</sup>,10<sup>−19</sup>,…,10<sup>−1</sup>,1,10,…,10<sup>19</sup>,10<sup>20</sup>}, and computes and outputs <em>x</em>, the respective values of <em>f </em>using the original expression, as well as your proposed (more stable) expression, the respective condition numbers (computed using the values of <em>f </em>with the original expression and the values of <em>f </em>with the proposed expression), and the relative error between the <em>f </em>values computed using the original and proposed expressions. Comment on the results. Use an appropriate format for the results, e.g. fprintf(’%9.2e %12.5e %12.5e %12.5e %12.5e %10.2e0, … <strong>2. </strong>Consider the integrals

<em>y<sub>n </sub></em><em><sup>n</sup>e</em><sup>−<em>t</em></sup><em>dt</em>,      <em>n </em>= 0, 1, 2,…

<ul>

 <li>[<em>10 points</em>] Derive a recurrence relation for <em>y<sub>n </sub></em>relating <em>y<sub>n </sub></em>to <em>y<sub>n</sub></em>−<sub>1</sub>. (You may have to use integration by parts.) Rearrange the formula so that you have a recurrence relation for <em>y<sub>n</sub></em>−<sub>1 </sub>relating <em>y<sub>n</sub></em>−<sub>1 </sub>to <em>y<sub>n</sub></em>. Name the first recurrence formula (A) and the second one (B).</li>

 <li>[<em>10 points</em>] With repeated applications of (A), give a formula that gives <em>y<sub>n </sub></em>as a function of <em>y</em><sub>0</sub>, i.e. <em>y<sub>n </sub></em>= <em>f<sub>n</sub></em>(<em>y</em><sub>0</sub>). With repeated applications of (B), give a formula that gives <em>y<sub>n </sub></em>as a function of <em>y<sub>m</sub></em>, for <em>m </em>&gt; <em>n</em>, i.e. <em>y<sub>n </sub></em>= <em>g<sub>n</sub></em><sub>,<em>m</em></sub>(<em>y<sub>m</sub></em>). (c) [<em>10 points</em>] Find the condition number of the functions</li>

</ul>

<em>f<sub>n</sub></em>(<em>y</em><sub>0</sub>) and <em>g<sub>n</sub></em><sub>,<em>m</em></sub>(<em>y<sub>m</sub></em>) for <em>m </em>&gt; <em>n</em>.

(Note: Function <em>f<sub>n </sub></em>has <em>y</em><sub>0 </sub>as the variable, and function <em>g<sub>n</sub></em><sub>,<em>m </em></sub>has <em>y<sub>m </sub></em>as the variable.)

Taking into account the condition numbers of the above two functions formulate a stable method for computing <em>y</em><sub>0</sub>, <em>y</em><sub>1</sub>,…, <em>y<sub>N</sub></em>, where <em>N </em>≥ 1 is giv en.

<ul>

 <li>[<em>10 points</em>] Write and run a MATLAB or equivalent program that computes and outputs <em>y</em><sub>0</sub>, <em>y</em><sub>1</sub>,…, <em>y<sub>N</sub></em>, starting with <em>y</em><sub>0 </sub>and using recursion (A). Explain what happens! (A reasonable <em>N </em>to stop is <em>N </em>= )</li>

 <li>[<em>15 points</em>] Write a MATLAB or equivalent program that sets <em>y<sub>N</sub></em>+<em><sub>K </sub></em>to some appropriate value (which may be approximate), and computes and outputs (<em>N </em>+ <em>K </em>− 1, <em>y<sub>N</sub></em>+<em><sub>K</sub></em>−<sub>1</sub>), (<em>N </em>+ <em>K </em>− 3, <em>y<sub>N</sub></em>+<em><sub>K</sub></em>−<sub>2</sub>),…,(<em>N</em>, <em>y<sub>N</sub></em>), starting with <em>y<sub>N</sub></em>+<em><sub>K </sub></em>and using recursion (B). At the end of the recursion, when the value of <em>y<sub>N </sub></em>is output, also output the ‘‘exact’’ value and the (absolute) error in the computed <em>y<sub>N</sub></em>. Run the program for <em>K </em>= 3,…,9 and <em>N </em>= 20 (7 cases). Note that the code should have a nested loop (one loop for <em>K </em>and one for the recursion). Explain what happens! Assume the ‘‘exact’’ value is q = 0.018350467697256206326; Comment on how one should compute <em>y</em><sub>20 </sub>to machine precision.</li>

</ul>

Notes: You should not use any symbolic environment. No integral calculations (other than the recurrences given). Use (the standard) double precision. You should not change the precision. Use an appropriate format, e.g. fprintf(’%3d %20.16f
’, i-1, y(i)); and fprintf(’%3d %20.16f %20.16f %10.6e
’, 20, y(21), q, qy(21));.

CSC336 Assignment 1      C. Christara – 2 –

<ol start="3">

 <li>[<em>15 points</em>] Assume that <em>A </em>and <em>B </em>are given dense <em>n </em>× <em>n </em>matrices, <em>B </em>is non-singular, II is the identity matrix of order <em>n</em>, and <em>b </em>a giv en <em>n </em>× 1 vector, for some <em>n </em>large. Explain how you would efficiently compute <em>z </em>= <em>B</em><sup>−1</sup>(2<em>A </em>+ II)(<em>B</em><sup>−1 </sup>+ <em>A</em>)<em>b</em>. Give, in terms of <em>n</em>, approximate operation counts for all computations you propose.</li>

</ol>

<em>Note</em>: The computations that you will propose may include LU factorization, back-and-forward substitutions, matrixvector products, matrix-matrix products, matrix inverse calculation, addition of vectors or matrices, and other similar computations. However, you are <strong>not </strong>obliged to use <strong>all </strong>these types of computations. For each computation you propose, you should give operation counts (indicating the highest power of <em>n</em>, including the coefficient), and make sure that the total number of operation counts is as little as possible. You do <strong>not </strong>need to describe algorithms for these computations. Also note that, while <em>B </em>is given, <em>B</em><sup>−1 </sup>is not given.

CSC336                                                                                Assignment 1                                    C. Christara