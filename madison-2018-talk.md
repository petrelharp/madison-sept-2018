---
title: "Landscapes of linked selection" 
subtitle: "(and how to simulate them)"
author: "Peter Ralph"
date: "Madison // Laboratory of Genetics // September 2018"
---




# Overview

##

1. *Theory:* a field guide to linked selection
2. *Practice:* some landscapes from the wild
3. *Simulation:* recent progress on a hard problem

## Genomic landscapes


![Langley et al 2012](figs/from_the_literature/langley-et-al-2012-chr3-pi-and-rho.png)


##


What causes variation in genetic diversity?



##

$$
\begin{aligned}
\pi &= \text{ (within-pop diversity) } \\
d_{xy} &= \text{ (between-pop divergence) } \\
F_{ST} &= \text{ (relative differentiation) }
\end{aligned}
$$

::: {.centered}

![](figs/fst_tree.png){width=60%}

:::

<!-- section THEORY -->

# Linked selection, in theory

--------------

linked selection

: The indirect effects of selection on genomic locations
  that are *linked* to the sites under selection by a lack of recombination.

::: {.centered}

![](figs/sweep_haps.png){.fragment width="40%"}
![](figs/background_haps.png){.fragment width="40%"}

:::

--------------------

**Linked Selection: a field guide**

*composed of rough sketches*

. . .

*citations: numerous*

0. Neutrality
-------------

![](figs/linked-selection-guide/linked-selection-site-neutral_early.png)

0. Neutrality
-------------

![](figs/linked-selection-guide/linked-selection-site-neutral.png)


1. A "hard" sweep
-----------------

![](figs/linked-selection-guide/linked-selection-site-hard.png)

2. A "soft" sweep
-----------------

![](figs/linked-selection-guide/linked-selection-site-soft.png)

3. Adaptive introgression
-------------------------

![](figs/linked-selection-guide/linked-selection-site-introgression.png)

4. Local adaptation with gene flow
-------------------

![](figs/linked-selection-guide/linked-selection-site-local_adaptation.png)

<!-- [Bierne 2010](https://doi.org/10.1111%2fj.1558-5646.2010.01050.x) -->

5. Background selection
-----------------------

![](figs/linked-selection-guide/linked-selection-region-background.png)

6. Recurrent sweeps
-------------------

![](figs/linked-selection-guide/linked-selection-region-recurrent_sweeps.png)

7. Recurrent introgression
--------------------------

![](figs/linked-selection-guide/linked-selection-region-recurrent_introgression.png)

## Etcetera

8. Recent balanching selection

9. Long-term balancing selection

10. Recurrent local adaptation after a split

11. Recurrent, transient balancing selection

12. All of the above?


<!-- section PRACTICE -->

# Linked selection, in practice


<!--
## *Homo sapiens*

![Hernandez et al 2011](figs/from_the_literature/hernandez-2011-dip-in-diversity.png)

*Hernandez et al 2011*
-->

## Diversity correlates with recombination rate

![Corbett-Detig et al](figs/from_the_literature/corbett-detig-divergence-recomb-drosophila.png)

Corbett-Detig et al 2015; Cutter & Payseur 2013 

--------------------

![Corbett-Detig et al](figs/from_the_literature/corbett-detig-divergence-recomb-all-species.png){width=70%}

Corbett-Detig et al 2015

-------------------

![Langley et al 2012](figs/from_the_literature/langley-et-al-2012-chr3-pi-and-rho.png)

<!--
-------------------

![McVicker et al 2009](figs/from_the_literature/mcvicker-2009-hu_chr1-landscape.png)
![](figs/from_the_literature/mcvicker-2009-hu_chr1-landscape-caption.png)

McVicker et al 2009
-->

<!-- AURENTIACUS -->

# How do genetic landscapes change over time?


The *Mimulus aurantiacus* species complex
-----------------------------------------

::: {.centered}
![](figs/aurantiacus/phylogeny.png)
:::


------------------

::: {.centered}
![](figs/aurantiacus/stankowski-color-cline.png){width=70%}
:::

----------------------------------

![https://www.biorxiv.org/content/early/2018/06/21/342352](figs/aurantiacus/preprint.png)

----------------------------------

![https://www.biorxiv.org/content/early/2018/06/21/342352](figs/aurantiacus/preprint_peeps.png)



-------------------------

The data:

- chromosome-level genome assembly
- $20\times$ coverage of 8 taxa and outgroup (*M.clevelandii*)
- diversity ($\pi$), divergence ($d_{xy}$),
    and differentiation ($F_{ST}$) in windows
- 36 pairwise comparisons among 9 taxa
- estimates of recombination rate and gene density
    from map and annotation

<!--
## A spectrum of differentiation

![](figs/aurantiacus/distributions.png)
-->

-------------------

![](figs/aurantiacus/lg1.png)


---------------------

![](figs/aurantiacus/emergence_of_fst_0.png)

---------------------

![](figs/aurantiacus/emergence_of_fst_1.png)

---------------------

![](figs/aurantiacus/emergence_of_fst_2.png)


---------------------

![](figs/aurantiacus/PUN_AUS_fst.png)

---------------------

![](figs/aurantiacus/PUN_CAL_fst.png)

---------------------

![](figs/aurantiacus/PUN_LON_fst.png)

---------------------

![](figs/aurantiacus/PUN_AUR_fst.png)

---------------------

![](figs/aurantiacus/PUN_FLE_fst.png)

---------------------

![](figs/aurantiacus/PUN_ARI_fst.png)

---------------------

![](figs/aurantiacus/PUN_BIF_fst.png)

---------------------

![](figs/aurantiacus/PUN_CLV_fst.png)


---------------------

![](figs/aurantiacus/cor-across-time-0.png)

---------------------

![](figs/aurantiacus/cor-across-time-1.png)

---------------------

![](figs/aurantiacus/cor-across-time-2.png)


## Conclusions

- Emergence of landscape of diversity across $\approx$ 1.5 million years!

- Shared targets of linked selection across taxa?

. . .

- But, what *kind* of linked selection? \
    How strongly and frequently does it act? \
    On how many targets?

. . .

Consequences for: genetic load/disease,
speed of evolution,
trait architecture.


<!-- section SIMULATION -->

# Simulation: not as easy as you might think

-----------------------------------------

![](figs/aurantiacus/phylogeny.png)

------------------

![](figs/aurantiacus/stankowski-color-cline.png){width=70%}


-----------------------------

To check predictions, we need simulations with:

- many loci under selection
- geographic population structure
- large populations with long genomes

for long enough to reach equilibrium ($\sim 10N$ generations).

. . .

For instance: $10^4$ individuals with $2 \times 10^8$ base pairs each for $10^5$ generations;
nonneutral mutations possible at $10^5$ loci.


##

*First:*

- **large populations with long genomes**


<!-- 1. explain tree sequences and why they are so efficient (5min) -->

# The tree sequence

---------------

![](figs/treseq_preprint.png)

---------------

![](figs/treseq_preprint_peeps.png)


## History is a sequence of trees

For a set of sampled chromosomes,
at each position along the genome there is a genealogical tree
that says how they are related.

![Trees along a chromosome](figs/sim_ts.anim.gif)


----------------------

A **tree sequence** describes this, er, sequence of trees.

<!--
. . .

*Observations:*

1. The *pedigree* (parental relationships) plus crossover locations
    would give us the tree sequence for *everyone, ever*.

2. Much less can fully describe the history relevant to a *sample* of genomes.

3. This information is equivalent to the Ancestral Recombination Graph (ARG).
-->


-------------

[Kelleher, Etheridge, and McVean](http://journals.plos.org/ploscompbiol/article?id=10.1371/journal.pcbi.1004842) 
introduced the **tree sequence** data structure
for a fast coalescent simulator, [msprime](https://github.com/jeromekelleher/msprime).

- stores genealogical *and* variation data **very** compactly

- efficient algorithms available:

    * subsetting
    * calculation of allele frequencies in arbitrary cohorts
    * linkage disequilibrium
    * log-time haplotype matching

- tree-based sequence storage closely related to haplotype-matching compression


## Simulated file sizes

::: {.columns}
::::::: {.column width="50%"}

![file sizes](figs/file_size.png)

:::
::::::: {.column width="50%"}

- HapMap chr1 genetic map (250Mb)
- Gutenkunst et al out-of-Africa model (3 pops)
- mutation rate $2 \times 10^{-8}$ per gen
- at $n=10^7$ 

    * about 17 million variants
    * VCF size: 318 TiB (250,000$\times$ larger)

:::
:::::::

## Example: three samples; two trees; two variant sites

![Example tree sequence](figs/example_tree_sequence.png)

-----------------------

Storing a tree sequence in
the four tables - *nodes*, *edges*, *sites*, and *mutations* -
is *succinct* (no redundancy).

. . .

These are stored efficiently on disk
with a bit more information (e.g., metadata).


## Nodes and edges

Edges 

:   Who inherits from who; only *necessary* for coalescent events.

    Records: interval (left, right); parent node; child node.

Nodes 

:   The ancestors those happen in.

    Records: time ago (of birth); ID (implicit).

-------------------

![Building a tree sequence](figs/nodes_edges_walkthrough/nodes_edges_walkthrough.0.png)

-------------------


![Building a tree sequence](figs/nodes_edges_walkthrough/nodes_edges_walkthrough.1.png)

-------------------


![Building a tree sequence](figs/nodes_edges_walkthrough/nodes_edges_walkthrough.2.png)

-------------------


![Building a tree sequence](figs/nodes_edges_walkthrough/nodes_edges_walkthrough.3.png)

-------------------


![Building a tree sequence](figs/nodes_edges_walkthrough/nodes_edges_walkthrough.4.png)

-------------------


![Building a tree sequence](figs/nodes_edges_walkthrough/nodes_edges_walkthrough.5.png)

-------------------

![Building a tree sequence](figs/nodes_edges_walkthrough/nodes_edges_walkthrough.6.png)


## Sites and mutations

Mutations

:   When state changes along the tree.

    Records: site it occured at; node it occurred in; derived state.

Sites 

:   Where mutations fall on the genome.

    Records: genomic position; ancestral (root) state; ID (implicit).


------------------

![Adding mutations](figs/sites_muts_walkthrough/sites_muts_walkthrough.0.png)

------------------

![Adding mutations](figs/sites_muts_walkthrough/sites_muts_walkthrough.1.png)

------------------

![Adding mutations](figs/sites_muts_walkthrough/sites_muts_walkthrough.2.png)

------------------

![Adding mutations](figs/sites_muts_walkthrough/sites_muts_walkthrough.3.png)

------------------

![Adding mutations](figs/sites_muts_walkthrough/sites_muts_walkthrough.4.png)



<!-- 4. explain application to fwds sim recording (5min) -->

# Forwards-time tree sequence recording

## The main idea

If we *record the tree sequence*
that relates everyone to everyone else,

after the simulation is over we can put neutral mutations down on the trees.

. . .

Since neutral mutations don't affect demography,

this is *equivalent* to having kept track of them throughout.

------------

This means recording the entire genetic history of **everyone** in the population, **ever**.

.  . .

It is *not* clear this is a good idea.


## Tree recording strategy

Every time an individual is born, we must:

::: incremental

1. add each gamete to the Node Table,
2. add entries to the Edge Table
    recording which parent each gamete inherited each bit of genome from, and
3. add any new selected mutations to the Mutation Table 
    and (if necessary) their locations to the Site Table.

:::

. . .

::: {.columns}
:::::: {.column width=15%}

![Rightarrow](figs/finger_right.png){width="100%"}

:::
:::::: {.column width=5%}

:::
:::::: {.column width=75%}

This produces **waaaaay** too much data.

:::
::::::

-------------------

We won't end up needing the *entire* history
of *everyone ever*,

. . .

but we won't know *what* we'll need until later.

. . .

How do we get rid of the extra stuff?


## Simplification

*Question:* given a tree sequence
containing the history of many individuals,
how do we *simplify* it to only the history
of a subset?

-----------

Concretely, given an input tree sequence
and a subset of its nodes we call the *samples*,

we want a new *minimal* tree sequence
that contains the history of those samples.

<!--
1. All marginal trees match the corresponding subtree 
    in the input tree sequence.

2. Every non-sample node in marginal trees has at least two children.

3. All nodes and edges are ancestral to at least one sample.

4. No adjacent redundant edges 
    (e.g., $(\ell, x, p, c) + (x, r, p, c) \rightarrow (\ell, r, p, c)$).
-->

-----------

To simplify a tree sequence
to the history of the *samples*:

> 1. Paint each *sampled* chromosome a distinct color.
> 
> 2. Moving back up the tree sequence,
>     copy colors of each chromosome to the parental chromosomes
>     they inherited from.
> 
> 3. If two colors go in the same spot (*coalescence*),
>     replace with a new color (unique to that ancestor).
>     Output a node for the ancestor and an edge for the coalescence.
> 
> 4. Once all colors have coalesced in a given segment,
>     stop propagating it.

## An example: simplify these to J and K

![Simplify example](figs/simplify_walkthrough.png){ width="100%" }

-------------------

![Simplify example](figs/simplify_walkthrough/simplify_walkthrough.0.png){ width="100%" }

-------------------

![Simplify example](figs/simplify_walkthrough/simplify_walkthrough.1.png){ width="100%" }

-------------------

![Simplify example](figs/simplify_walkthrough/simplify_walkthrough.2.png){ width="100%" }

-------------------

![Simplify example](figs/simplify_walkthrough/simplify_walkthrough.3.png){ width="100%" }

-------------------

![Simplify example](figs/simplify_walkthrough/simplify_walkthrough.4.png){ width="100%" }

-------------------

![Simplify example](figs/simplify_walkthrough/simplify_walkthrough.5.png){ width="100%" }

-------------------

![Simplify example](figs/simplify_walkthrough/simplify_walkthrough.6.png){ width="100%" }

-------------------

![Simplify example](figs/simplify_walkthrough/simplify_walkthrough.7.png){ width="100%" }

-------------------

![Simplify example](figs/simplify_walkthrough/simplify_walkthrough.8.png){ width="100%" }

-------------------

![Simplify example](figs/simplify_walkthrough/simplify_walkthrough.9.png){ width="100%" }

-------------------

![Simplify example](figs/simplify_walkthrough/simplify_walkthrough.10.png){ width="100%" }

-------------------

![Simplify example](figs/simplify_walkthrough/simplify_walkthrough.11.png){ width="100%" }

-------------------

![Simplify example](figs/simplify_walkthrough/simplify_walkthrough.12.png){ width="100%" }

-------------------

![Simplify example](figs/simplify_walkthrough/simplify_walkthrough.13.png){ width="100%" }

-------------------

![Simplify example](figs/simplify_walkthrough/simplify_walkthrough.14.png){ width="100%" }

-------------------

![Simplify example](figs/simplify_walkthrough/simplify_walkthrough.15.png){ width="100%" }


## Wright-Fisher, N=10: before simplification

![Wright-Fisher tree sequence](figs/sim_wf.anim.gif)

## Wright-Fisher, N=10: before simplification

![Wright-Fisher tree sequence](figs/sim_wf_unlabeled.anim.gif)

## ... and after simplification

![Simplified Wright-Fisher tree sequence](figs/sim_wf_simplified.anim.gif)


## *Revised* tree recording strategy

Every time an individual is born, we must:


1. add each gamete to the Node Table,
2. add entries to the Edge Table
    recording which parent each gamete inherited each bit of genome from
3. add any new mutations to the Mutation Table 
    and (if necessary) their locations to the Site Table.

... and,

4. Every so often, *simplify* the tables so far,
    retaining the history of the current generation.



# Implementation and results

## Benchmark implementation

- Recording, simplifying, and output of tables: 
    `C` code in `msprime`.

- Simulation: [`fwdpp`](https://github.com/molpopgen/fwdpp), by Kevin Thornton (in `C++`) ([code](https://github.com/molpopgen/fwdpy11_arg_example))

- Glue: [`pybind11`](https://github.com/pybind/pybind11/) and [`numpy`](http://www.numpy.org/)

- Machine: Ubuntu / 2x 2.6 GHz Intel E5-2650 CPU


## Simulation parameters


- Wright-Fisher population of size $N$

- simulated for $10N$ generations

- neutral mutation rate $\mu$ equal to recombination rate $r$ per gamete

- many, weakly deleterious mutations: rate $\mu/100$ with
    $s$ exponentially distributed with mean $2.5/N$.

. . .

*Note:*
if we recorded tree sequences ("pedigree recording")
then the neutral mutation rate was *zero*
but neutral mutations were added *afterwards*.


--------------------------

<!--
Translation:
$$
\begin{aligned}
N=10^3 \text{ and } \rho=10^4 \\
\Rightarrow L \approx 2.5 \times 10^8 \text{bp}
\end{aligned}
$$

$$
\begin{aligned}
N=10^4 \text{ and } \rho=10^4 \\
\Rightarrow L \approx 2.5 \times 10^7 \text{bp}
\end{aligned}
$$

$$
\begin{aligned}
N=5 \times 10^4 \text{ and } \\
\qquad \rho=10^5 \\
\Rightarrow L \approx 5 \times 10^7 \text{bp}
\end{aligned}
$$
-->

![Total run time per single simulation as a function of region length.](figs/rawspeed.png){ width=80% }

--------------------------

![Relative speedup of simulations](figs/speedup.png){ width=80% }


# Geographic simulations

----------------

To check predictions, we **still** need simulations with:

- many loci under selection
- **geographic population structure**
- large populations with long genomes

for long enough to reach equilibrium ($\sim 10N$ generations).

. . .

::: {.columns}
:::::: {.column width=15%}

![Rightarrow](figs/finger_right.png){width="100%"}

:::
:::::: {.column width=5%}

:::
:::::: {.column width=75%}

SLiM v3.1 *(Haller and Messer)*

:::
::::::

## 

::: {.columns}
::::::: {.column width="50%"}


**S**election on **Li**nked **M**utations, v3.1:
a forwards-time, individual-based, explicitly genomic simulator,
now with:

- continuous space
- geographic maps
- locally, density-dependent demography (*non-Wright-Fisher*)

:::
::::::: {.column width="50%"}

![](figs/slim_logo.png)
<!-- ![](figs/slim_space.png) -->

:::
:::::::

. . .

**And a GUI!!!**




## ... now with tree sequence recording!


![](figs/slim_preprint.png)


## A 100x speedup:

::: {.centered}
![](figs/slim_timing.png){width=60%}
:::

## What else can you do with the tree sequence?

> - record ancient samples 
> - true ancestry reconstruction 
> - *recapitation*: fast, post-hoc initialization with coalescent simulation 


---------------------

**For example:**


- genome as human chr7 ($1.54 \times 10^8$bp)
- $\approx$ 10,000 diploids
- 500,000 overlapping generations
- continuous, square habitat
- selected mutations at rate $10^{-10}$
- neutral mutations added afterwards

*Runtime:* 8 hours

---------------------

**Sweeps and background selection**:
$$
    \pm s \sim \text{Gamma}(2, \text{mean}=0.005)
$$

![](figs/slim_divergences_run_031486.png)


---------------------

**Sweeps and background selection**:
$$
    \pm s \sim \text{Gamma}(2, \text{mean}=0.005)
$$

![](figs/slim_divergences_run_031486_shaded.png)

---------------------

**Local adaptation**:

$s$ as above but beneficial on one side, deleterious on the other

![](figs/slim_divergences_run_016913.png)


---------------------

**Local adaptation**:

$s$ as above but beneficial on one side, deleterious on the other

![](figs/slim_divergences_run_016913_shaded.png)



# Summary

-------

> - Landscapes of genetic diversity are clues to the ongoing types and intensities
    of natural selection.

> - We can see them emerge, and change with time.

> - What makes these landscapes? Still unknown.

> - But, we can finally simulate the process!

> - Tree sequences are awesome.



Thanks!
-------

Mimulus: Madeline Chase, Sean Stankowski, Matt Streisfeld

Tree sequences: Jerome Kelleher, Ben Haller, Jaime Ashander, Kevin Thornton, Jared Galloway

Funding: NSF ABI, Sloan, UO

Slides with [reveal.js](http://hakim.se) and [pandoc](https://pandoc.org/).


<!-- MISCELLANEA -->

##

miscellanea


Hitchhiking
-----------

![Maynard Smith & Haigh](figs/from_the_literature/maynard-smith-haigh-hitchhiking-dip.png)


Background selection
--------------------

![Hudson 1994](figs/from_the_literature/hudson-1994-background-dip-in-diversity.png)


Balanced polymorphism
---------------------

![Kreitman & Hudson 1991](figs/from_the_literature/kreitman-hudson-fig-5.png)


3. Recent balancing selection
----------------------

![](figs/linked-selection-guide/linked-selection-site-recent_balancing.png)


4. Long-term balancing selection
----------------------

![](figs/linked-selection-guide/linked-selection-site-old_balancing.png)


## *Drosophila melanogaster*

![McGaugh et al 2012](figs/from_the_literature/mcgaugh-2012-drosophila-dip.png)



---------------------

![](figs/aurantiacus/diversity-recomb.png)


------------------

![](figs/aurantiacus/correlations.png){width=70%}

------------------

Simplification finds the minimal tree sequence,
for a subset of its samples, such that:

1. All marginal trees match the corresponding subtree 
    in the input tree sequence.

2. Every non-sample node in marginal trees has at least two children.

3. All nodes and edges are ancestral to at least one sample.

4. No adjacent redundant edges 
    (e.g., $(\ell, x, p, c) + (x, r, p, c) \rightarrow (\ell, r, p, c)$).

