# Problem Set 8: DNA in a nucleus
Jun Allard

DNA in eukaryotic cells is packed by complex machinery inside the
nucleus. Here, will use the ideal chain model to explore the need for
this machinery by studying what would happen if the DNA were not
carefully packed, i.e., by assuming it is just a freely-jointed chain
randomly packed in a spherical nucleus.

1.  Find the following quantities. Cite your sources.

    - The total length of DNA of a typical human chromosome, $l$,
    - The size (roughly the diameter) of a typical eukaryotic nucleus,
      $D$,
    - The width of double-stranded DNA, $w$.
    - The persistence length of double-stranded DNA, $l_p$.

We will use these quantities to estimate how big a chromosome is, first
from the point-of-view of occupation fraction, then from the
point-of-view of polymer physics.

2.  Assume DNA is a long cylinder of width $w$ and length $l$. What is
    the total volume of DNA in each cell? You may assume a single
    chromosome.
3.  Assuming the nucleus is spherical, what fraction of the volume of
    the nucleus is occupied by DNA?

For the remainder of the problem, you may use order-of-magnitude
precision.

The end-to-end distance $r_{ee}$ of a flexible polymer satisfies the
probability distribution

$$p(r_{ee}) = 4\pi r_{ee}^2 \left( \frac{3}{2\pi l\,l_p}\right)^{\frac{3}{2}} \exp\left(\frac{-3r_{ee}^2}{2l\,l_p}\right).$$

If a system explores macrostates parametrized by $r$, and in the absence
of confinement or external forces has probability distribution $p(r)$,
then the entropy of macrostate $r$ is

$$S(r) = k_B \ln \left( p(r)\right) + S_0$$

where $S_0$ is a constant that is independent of the system’s state.
(Eventually, only derivatives of $S(r)$ matter for forces and pressures,
so these should be independent of $S_0$.)

If a polymer is confined to a sphere of diameter $D$, this would mean
the maximum distance between any two nodes, $r_\mathrm{max}$, is less
than $D$. Therefore, to be rigorous, computing the force a polymer
exerts by this confinement would require the probability distribution
$p_\mathrm{max}(r_\mathrm{max})$. Unfortunately we do not have an
expression for $p_\mathrm{max}(r_\mathrm{max})$. Let us instead make an
approximation that there exists a characteristic polymer “size” $r$ such
that $r \sim r_{ee} \sim r_\mathrm{max}$.

4.  Write an expression for the free energy $G = -T S$ as a function of
    polymer size $r$.
5.  Pressure is force per unit area. Find an expression for the outward
    pressure exerted by the polymer if it is confined to a sphere of
    radius $r=R$.
6.  Use your findings to estimate the pressure exerted by DNA inside the
    nucleus, if it were randomly packed. Report your value in units of
    atmospheres (1 atmosphere $\approx 10^5$ Pascals).
7.  We wish to answer the question: is the pressure you found in (vi)
    sufficient to rupture the nucleus? What number should this pressure
    be compared with? Look up this number and make this comparison.
