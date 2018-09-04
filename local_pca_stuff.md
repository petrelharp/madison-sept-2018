
<!--  LOCAL PCA -->

# Tree *shape*: with local PCA


## Principal Components Analysis (PCA)

![van Heerwaarden et al 2010](figs/maize_pca.jpg)

<!-- http://www.pnas.org/content/108/3/1088.full -->

----------------

![Novembre et al 2008](figs/novembre-map-genes-mirror-geography-crop.jpg)


## PCA describes the covariance matix

Genetic covariance between samples $i$ and $j$ is
the average over loci
and reference samples $x$, $y$ of:

::: {.center}

![](figs/what_is_covariance.png)

:::

... so summarizes average *patterns of relationships*
caused by *population structure*.


## Population structure

... is historical patterns of interbreeding, migration, and population sizes.

. . .

but: linked selection

**locally distorts** genealogical patterns.

**Question:** is there significant *shared* variation
in patterns of relatedness?


---------------

![Our method](figs/the-method-diagram-modified.png)



## `lostruct`

:::::::::::::: {.columns}
::: {.column width="50%"}

 * an R package
 * with templated Rmarkdown reports
 * and a script interface
 * [https://github.com/petrelharp/local_pca](https://github.com/petrelharp/local_pca)

:::
::: {.column width="50%"}

![](figs/the-method-diagram-modified.png)


:::
::::::::::::::


## Data: African *D. melanogaster*

:::::::::::::: {.columns}
::: {.column width="50%"}

![](figs/drosophila_2R_inversion_pcs_0.png)

:::
::: {.column width="50%"}

* DPGP *(Langley et al 2012; Pool et al 2012; Lack et al 2015)*
* 380 mostly African samples -- WGS -- 9 Kb windows

:::
::::::::::::::


------------

![](figs/drosophila_2R_inversion_pcs_1.png)

* large, segregating inversions *(Corbett-Detig & Hartl 2012; Langley et al 2012)*

------------

![](figs/drosophila_recomb_mds_for_talk.png)

* without less common inversion haplotypes: *linked selection?*


## Data: *Medicago truncatula* Hapmap (Tang et al 2014)

* 263 pan-Mediterranean samples -- WGS -- 100 Kb windows

##

![](figs/medicago_for_talk.png)



## 

**Patterns are not driven by:**

* recombination rate variation
* polymorphism
* PC switching
* missingness


## {.center}

So, which is it?

. . .


? ? ?

----------------


