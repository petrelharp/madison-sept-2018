.PHONY : figs linked_selection_figs local_pca_figs aurantiacus_figs

figs : linked_selection_figs local_pca_figs aurantiacus_figs fst_tree.png background_haps.png sweep_haps.png slim_timing.png slim_space.png slim_logo.png from_the_literature/langley-et-al-2012-chr3-pi-and-rho.png slim_divergences_run_031486.png slim_divergences_run_031486_shaded.png slim_divergences_run_016913.png slim_divergences_run_016913_shaded.png 
	
linked_selection_figs : linked-selection-guide/linked-selection-site-neutral.png linked-selection-guide/linked-selection-site-neutral_early.png linked-selection-guide/linked-selection-site-hard.png linked-selection-guide/linked-selection-site-soft.png linked-selection-guide/linked-selection-site-recent_balancing.png linked-selection-guide/linked-selection-site-old_balancing.png linked-selection-guide/linked-selection-site-introgression.png linked-selection-guide/linked-selection-site-local_adaptation.png linked-selection-guide/linked-selection-region-background.png linked-selection-guide/linked-selection-region-recurrent_sweeps.png linked-selection-guide/linked-selection-region-recurrent_introgression.png

local_pca_figs : what_is_covariance.png drosophila_2R_inversion_pcs_0.png drosophila_2R_inversion_pcs_1.png drosophila_recomb_mds_for_talk.png medicago_for_talk.png the-method-diagram-modified.png

aurantiacus_figs : aurantiacus/phylogeny.png aurantiacus/distributions.png aurantiacus/diversity-recomb.png aurantiacus/correlations.png aurantiacus/lg1.png aurantiacus/building_cor_1.png aurantiacus/building_cor_2.png aurantiacus/building_cor_3.png aurantiacus/building_cor_4.png aurantiacus/cor-across-time-0.png aurantiacus/cor-across-time-1.png aurantiacus/cor-across-time-2.png aurantiacus/stankowski-color-cline.png aurantiacus/emergence_of_fst_0.png aurantiacus/emergence_of_fst_1.png aurantiacus/emergence_of_fst_2.png

linked-selection-guide/linked-selection-site-%.pdf : linked-selection-guide.ink.svg
	./export-layers-svg.sh $< axes site $* >$@

linked-selection-guide/linked-selection-region-%.pdf : linked-selection-guide.ink.svg
	./export-layers-svg.sh $< axes region $* >$@

aurantiacus/building_cor_%.pdf : aurantiacus/building_cor.ink.svg
	./export-layers-svg.sh $< building_cor_$* >$@

aurantiacus/cor-across-time-%.pdf : aurantiacus/cor-across-time.ink.svg
	./export-layers-svg.sh $< layer$* >$@

aurantiacus/emergence_of_fst_%.pdf : aurantiacus/emergence_of_fst.ink.svg
	./export-layers-svg.sh $< axis time$* >$@

slim_divergences_%.pdf : slim_divergences.ink.svg
	./export-layers-svg.sh $< $* >$@

slim_divergences_%_shaded.pdf : slim_divergences.ink.svg
	./export-layers-svg.sh $< $* shading >$@

## image conversion

%.pdf : %.svg
	inkscape $< --export-pdf=$@

# %.svg : %.pdf
# 	inkscape $< --export-plain-svg=$@

%.png : %.pdf
	convert -density 300 $< -flatten $@

%.gif : %.pdf
	convert -density 300 $< -flatten $@

%.png : %.svg
	convert -density 300 $< -flatten $@

%.gif : %.svg
	convert -density 300 $< -flatten $@

%.pdf : %.ink.svg
	inkscape $< --export-pdf=$@

# animated gif
%.anim.gif : $(wildcard %/*.gif)
	convert -loop 0 -delay 10 -coalesce -fuzz 2% -layers optimize $$(ls $*/*.gif) $@
