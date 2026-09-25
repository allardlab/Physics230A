# Problem Set 7: Inferring methyltransferase binding rates
Jun Allard

Suppose a system can transition between two states, State 1 and State 2,
with transition rates $k_{1\rightarrow 2}$ and $k_{2\rightarrow 1}$. If
transitions are driven by thermal fluctuations, then these transition
rates must obey

<span id="eq-detailed-balance-2">
$$\frac{k_{1\rightarrow 2}}{k_{2\rightarrow 1}} = e^{-(E_2-E_1)/k_BT} = e^{-(\Delta E_{12})/k_BT}
 \qquad(1)$$</span>

where $E_1$ and $E_2$ are the energies of those two states.

If a system can transition between 3 states, State A, State B and State
C, and transitions are driven by thermal fluctuations, then it follows
from <a href="#eq-detailed-balance-2" class="quarto-xref">Equation 1</a>
that

<span id="eq-detailed-balance-3">
$$\frac{k_{A\rightarrow C}}{k_{C\rightarrow A}} = \frac{k_{A\rightarrow B}}{k_{B\rightarrow A}} \cdot \frac{k_{B\rightarrow C}}{k_{C\rightarrow B}}.
 \qquad(2)$$</span>

This means that, to find all 6 transition rates, an experimentalist
would only need to measure 5 rates. The sixth (whichever it is) could
then be computed from
<a href="#eq-detailed-balance-3" class="quarto-xref">Equation 2</a>.

## A.

A methyltransferase called DNMT loads a methyl group (from S-Adenosyl
methionine), binds to DNA, and attaches the methyl to the DNA. This is a
form of epigenetic regulation that plays a role in cell fate
determination[^1] Thus, it can exist in 4 states: bound or unbound to
DNA, carrying or not carrying a methyl.

<img src="fig_methyltransferase-rates.svg" style="width:10cm"
data-fig-align="center"
data-fig-alt="A two-by-two diagram of the four states of the methyltransferase DNMT. Top left, state 1: the enzyme is free of the DNA and carries no methyl group. Top right, state 2: the enzyme is still free but now carries a methyl. Bottom left, state 3: the enzyme is bound to the DNA and carries no methyl. Bottom right, state 4: the enzyme is bound to the DNA and carries a methyl. Eight arrows connect the states around the square: k12 and k21 across the top, k34 and k43 across the bottom, k13 and k31 down the left side, and k24 and k42 down the right side. The two diagonal transitions are absent." />

Suppose that only one binding/unbinding event or loading/unloading event
can occur at a time, in which case only the 8 transitions shown in the
diagram are allowed (i.e., you may assume the 4 “diagonal” transitions
have zero rate).

1.  The rate constraint equation above for 3-states,
    <a href="#eq-detailed-balance-3" class="quarto-xref">Equation 2</a>,
    is a constraint purely involving rates ($k$’s) and no state energies
    or probabilities. For the 4-state system, find all constraints on
    the rates that only involve rates ($k$, no state energies or
    probabilities) that are produced by the Principle of Detailed
    Balance.
2.  How many are there? And therefore, how many independent rates must
    the experimentalist measure?

## B.

Suppose a system can transition between $N$ states, $i=1..N$. There are,
in general, $N\cdot(N-1)$ transition rates. If the system obeys Detailed
Balance, how many constraints are there? And therefore, how many
independent rates must an experimentalist measure? Note that in Part A,
we assumed that there were 4 states and only 8 non-zero transitions,
whereas in general, a 4-state system has 12 transitions.

[^1]: L. Busto-Moner, J. Morival, H. Ren, A. Fahim, Z. Reitz, T. L.
    Downing, E. L. Read. Stochastic modeling reveals kinetic
    heterogeneity in post-replication DNA methylation. PLOS
    Computational Biology (2020).
