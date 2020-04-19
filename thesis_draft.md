---
# Front matter
title:  "Identification of neural premotor substrates affecting nocifensive behaviour in Drosophila larvae"
author: |
	| Alastair Garner 
	| Supervisor: Dr. Tomoko Ohyama
	| Integrated Program in Neuroscience
date: | 
	| McGill University, Montreal
	| April 2020
	|
	|
	|
	| A thesis submitted to McGill University in partial fulfilment of the requirements of the degree of Master of Science
	| 
	| $\copyright$ Alastair Garner 2020
documentclass: article

# Bibliography
link-citations:  true
csl:
	- current-biology.csl
color-links: true
linkcolor: Blue

# Formatting
numbersections:
	- 1
secnumdepth:
	- 3
geometry: 
	- letterpaper
	- margin=1in
mainfont: 
	- "Palatino Linotype"
sansfont:
	- "Avenir LT Std"
fontsize:
	- 12pt
---

# Introduction

Neural circuitry must coordinate numerous aspects of a given behaviour, activating distinct motor cohorts in a stereotyped sequence, whilst integrating sensory feedback to modulate the performance of the behaviour. Understanding how the innate wiring of neural circuits underpins the generation of these coordinated motor patterns offers insight into general neural mechanisms for rhythmicity, patterning and action selection. This has motivated research, particularly in basal locomotor modes, into quadrapedal walking in the cat[@Kiehn2006a,@Nishimaru2009,@Buford1990] and mouse[@Crone2008e,@Grillner2009b,@Zagoraiou2009,@Dougherty2013,@Goetz2015,@Bikoff2016], swimming in fish[@Kimura2013a,@Song2016], leech[@Friesen2007] and lamprey[@Grillner2003,@Mullins2011], as well as crawling in *Drosophila* larva[@Heckscher2012,@Clark2018a,@Kohsaka2017] and *C. elegans*[@Wen2012a,@Piggott2011,@Zhen2015].

*Drosophila* larva are an excellent model system for studying locomotion given their genetic tractability, readily quantifiable behaviour[@Ohyama2013,@Kabra2013] and fully described somatic musculature[@Bate1990]. Each hemisegment of the ventral nerve cord (VNC, analogous to the vertebrate spinal cord) contains 250 interneurons[@Rickert2011] which are hardwired to coordinated different behavioural modes. Of these, the nocifensive behavioural repertoire of a *Drosophila* larva includes a corkscrew-like "rolling" behaviour[@Tracey2003] that demonstrates a distinct motor profile to that for peristaltic crawling[@Heckscher2012]. How distinct circuits are wired to coordinate mutually exclusive locomotor patterns through a common musculature remains an unanswered question.

Here we seek to identify novel premotor interneuron components for the performance for nocifensive behaviour in *Drosophila* larva. We will characterise the phenotypic contribution of these neurons to both escape behaviours and basal locomotion, to address whether premotor neurons exhibit behaviour specificity or promiscuity. Finally we will assay premotor neurons with similar anatomical connectivity to determine whether perturbation of common motor cohorts results in comparable phenotypes.



# Background
The review articles from Clark *et al*.[@Clark2018a] and Kohsaka *et al*.[@Kohsaka2017] were particularly useful for formulating the following section.



## *Drosophila* as a model system in neuroethology 

Use of *Drosophila* as a model system for studying neuroethology originates with the mutagenesis screenings conducted by Seymour Benzer and colleagues, where mutated flies were assayed for novel behavioural phenotypes and associated genes determined by genetic mapping[@Konopka1971]. This established the classic "Genes to Behaviour" dogma. The development of genetic tools to selectively express genes of interest in specific cell types (UAS-GAL4 system)[@Brand1993] allowed for increased accessibility of the system. This reached a head with the development of the split-GAL4 system[@Luan2006] which allowed restricted expression of exogenous genes to smaller populations of cells. This was exploited by Pfeiffer and colleagues[@Pfeiffer2010] and expanded upon by Jenett *et al*.[@Jenett2012] and others[@Gohl2011,@Li2014] who, collectively, have generated 1000's of split-GAL4 lines with expression patterns restricted to fly nervous system. 



Within neuroethology these tools allowed for the manipulation of neuronal activity, with the development of effector lines to inhibit[@Baines2001,@Paradis2001], silence[@Sweeney1995, @Kitamoto2001] and artificially activate[@Rosenzweig2005,@Rosenzweig2008] neuronal populations of interest. More recently the advent of optogenetics, where light activatable ion channels are expressed in neurons of interest, has allowed even greater temporal precision in activating[@Boyden2005] and inhibiting[@Mohammad2017] neurons. With expansion of the catalogue of available constructs to include wavelength-shifted variants of channelrhodopsin[@Klapoetke2014] the utility of optogenetics continues to be optimised.



In addition, genetically encoded calcium indicators (GECIs) have been developed to allow imaging of neuronal activity. These constructs, when expressed in a neuron population of interest, allow for visualisation of increases in internal calcium concentration - a proxy for bouts of neuronal activity. In particular *UAS-GCaMP*[@Wang2003], a split flourophore reconstituted by calcium binding, has become widely popular. This construct has since been iterated upon[@Chen2013a,@Dana2019], improving the temporal dynamics, sensitivity and signal-to-noise, allowing for single or population level neural recording with high temporal fidelity.



While much effort focuses on the adult fly, research on larval *Drosophila* has gained popularity for their reduced behavioural repertoire and comparatively small number of neurons (ca. 10,000, versus 100,000 in the adult). On top of this, larva have a translucent cuticle, simplifying the application of optogenetics and imaging of neuronal activity. Analytical tools have been adapted from *Caenorhabditis elegans* research[@Swierczek2011] to allow for the development of high-throughput behavioural assays in *Drosophila* larva[@Ohyama2013]. Likewise robust methods for behavioural quantification have also been developed based on user-curated behavioural definitions[@Ohyama2013], unsupervised hierarchical clustering[@Vogelstein2014] and supervised machine learning techniques[@Kabra2013,@Jovanic2017]. 



## *Drosophila* larval nocifensive behaviour

In their natural environment *Drosophila* are preyed upon by parasitoid wasps [@Carton1986] like those of the *Chalcidoidea* and *Ichneumonoidea* superfamilies. The female wasp inserts its sharp ovipositior through the larval cuticle and lays an egg. The developing wasp larva then digests the host *Drosophila* from the inside out, eventually resulting in the pupation and eclosion of a juvenile wasp. Parasitoid wasps produce a strong selective pressure on *Drosophila*[@Powell1997], which has lead to the evolution of endogenous mechanisms to fight the parasite. The first of these is a cellular immune response that can destroy the wasp egg, preventing the development of wasp and thus also the death of the *Drosophila* larva[@Rizki1990]. The other is a unique behavioural repertoire in which the *Drosophila* larva produces a stereotyped pattern of nocifensive behaviours. These consist of an initial C-shape bend, where the head and tail are simultaneously moved either to the left or right of the body axis[@Ohyama2013] ([@fig:repertoire]A), followed by a corkscrew-like "roll" motion where the larva rotates around the anteroposterior axis[@Tracey2003] ([@fig:repertoire]B). After first presentation these behaviours can repeat, but are typically concluded by a bout of "fast-crawling", where the animal crawls with an elevated frequency of peristalsis ([@fig:repertoire]C). The direction of a roll is dictated by the position at which the wasp ovipositor is inserted, such that the rotation of the larval body removes the ovipositor, preventing egg-laying[@Hwang2007]. In laboratory conditions rolling behaviour can be readily elicited by activation of the *painless* expressing class IV dendrite arborization (CIVda or MDIV) neurons, a class of nociceptors that respond to harsh mechanical stimulation[@Zhong2010], noxious temperatures[@Zhong2012] and strong UV light[@Xiang2010].



![**Escape repertoire of *Drosophila* larva.** (**A**) C-shape bend involves contraction of the head and tail in the same direction. (**B**) One complete roll represents a full 360 degree rotation around the anteroposterior body axis. (**C**) Fast crawling is biomechanicallly similar to normal crawling but with an increased frequency of peristalsis.](./bend_sequence.svg){#fig:repertoire}



## Neural circuitry for activation of nocifensive behaviour

Subsequent efforts have begun to elucidate the neural substrates downstream of these nociceptive neurons that facilitate the performance of larval nocifensive behaviour. Ohyama *et al*.[@Ohyama2015] produced a serial section transmission electron microscopy (ssTEM) volume for the brain of a first instar larva allowing them to trace all the downstream synaptic partners of the CIVda neurons. From this they were able to identify 13 distinct pairs of postsynaptic target neurons, based on morphology. In particular they identified a population of first-order interneurons, termed Basin neurons, that received input from both the CIVda and the mechanosensory chordotonal (Ch) neurons. Imaging these neurons illustrated they were functionally multisensory and that activation of Ch neurons using a vibration stimulus affected a multimodal enhancement on rolling behaviour. Activation of Basin or the disynaptic downstream neuron pair, Goro, was sufficient to induce the full escape repertoire.

A09l neurons, coined 'Down-and-Back' (DnB) neurons[@Burgos2018], have also been linked to the Goro-mediated roll pathway. A09l neurons receive monosynaptic input from both CIVda and gentle-touch receptor neurons, CIIda and CIIIda, and when activated were sufficient to elicit rolling behaviour. Notably activation of A09l was more likely to result in C-shape bending without a resultant roll than with a roll. Further, silencing Goro reduced the probability of observing rolling behaviour without impacting the likelihood of C-shape bending, suggesting that these two locomotor modes may in fact be under control via separable, modular motor programmes[@Burgos2018]. Goro was found to be three synapses downstream of A09l, leading the authors to conclude that A09l-mediated rolling behaviour was Goro-dependent. 

Other neuron populations have also been associated with larval nocifensive behaviour. Hu *et al*.[@Hu2017] characterised two further sets of second-order sensory neurons downstream of CIVda and involved in nocifensive behaviour: A08n, which had previously been previously linked to rolling[@Vogelstein2014] and a dorsal pair of insulin-like peptide 7 producing neurons (DP-ilp7). A08n was shown to be both necessary and sufficient to elicit rolling behaviour, whereas the DP-ilp7 neurons triggered a bending behaviour akin to the initial C-shape bend performed prior to rolling. DP-ilp7 neurons also received innervation from the low-threshold mechanoreceptor neuron CIIda and CIIIda[@Grueber2002,@Tsubouchi2012] suggesting, like Basins, these neurons may be integrating sensory information to gate the performance of rolling. Interestingly they also noted that activation of the CIIda mechanoreceptor, in the absence of CIVda nociceptor activation, was sufficient to trigger rolling behaviour, compounding the evidence that rolling involves the convergence of different sensory modalities.



![**Neural circuitry underlying nocifensive behaviour.** Neurons highlighted in red are sufficient, when activated, to elicit nocifensive behaviour. The musculature is grouped into transverse (LT) and longitudinal (DL,DO,VL,VO) muscles for simplicity. The downstream partners of Goro, A08n and DP-ilp7 are not known.](./circuit_map.svg){#fig:circuitry}

## Larval musculature

The somatic musculature of *Drosophila* larva is highly stereotyped and well described[@Bate1990]. Each abdominal hemisegment contains 30 muscles that can broadly be categorised by two groups: the longitudinal muscles which arrange in parallel with the body axis, or the transverse muscles which are circumferential to the body wall[@Bate1990,@Clark2018a] ([@fig:muscles]). Each of these 30 muscles are innervated by a single "big" bouton motor neuron (1b motor neurons), as well as a single "small" bouton (1s motor neuron) neuron that projects to each of the muscles within one of three functionally related groups (dorsal longitudinal, ventral longitudinal and transverse)[@Landgraf2006,@Peron2009]. These motor neurons provide glutamatergic, excitatory innervation of the muscles. Many 1b neurons show rhythmic activity coincident with waves of muscle contraction during both forward and backward locomotion[@Newman2017]. 

The contribution of somatic musculature to basal locomotion has been characterised by Heckscher *et al*.[@Heckscher2012], which established larvae as a model system for studying rhythmic behaviour. In describing the motor profile for peristaltic crawling, they identified a differential order of contraction for forward and reverse crawling modes. This has recently been supported by a study that used calcium imaging to image the activation of somatic muscles during forward and reverse crawls, allowing identification of different combinations of co-active muscles for either locomotor mode[@Zarin2019a].

No studies as of yet have addressed which muscles are active during or necessary for nocifensive C-bend or rolling behaviour. Coordination of these behaviours could be reliant on the recruitment of unique behaviour-specific muscles, similar to unifunctional muscles found in the crab/lobster[@Mulloney2014,@Bucher2006,@Briggman2008] and mollusk[@Popescu2002a]. However, given that all abdominal somatic muscles show activity during peristaltic crawling[@Zarin2019a] it is likely that such coordination is instead encoded by the neural premotor circuitry.

![**Larval musculature and motor neurons.** Lateral schematic of the somatic musculature of a single abdominal hemisegment. The muscles are arranged as per the cartoon larva (bottom-right), with the head to the left. The ventral nerve cord (VNC) is coloured dark grey. Each of the somatic muscles is innervated by a single big bouton (Ib) type motor neuron of same name. Common motor neuron pseudonyms are listed apposed to the numerical labels. Muscles are grouped anatomically by their position on the dorsolateral axis and their orientation.](./Thesis_musculature.svg){#fig:muscles}



## Motor coordination for *Drosophila* locomotion

To date, few studies have investigated neural circuits for motor coordination of nocifensive behaviours. However, given the shared musculature between these behaviours, insights from the coordination of other locomotor behaviours may well be relevant for the nocifensive repertoire.

### Transverse-linked circuitry

One group of muscles thought to be important for rolling behaviour are the lateral transverse (LT) muscles ([@fig:muscles]). The LT motor neurons projecting to these muscles were first assayed by Picao-Osorio *et al*.[@Picao-Osorio2015] who screened for neurons implicated in self-righting behaviour, in which upside-down larva must correct their dorsoventral orientation. Silencing the LT motor neurons resulted in a larva which, while dorsal-side down, could perform left-right bending but struggled to roll back onto their ventral side. This self-righting behaviour is visibly similar to nocifensive rolling and the two behaviours are presumed to share a similar motor profile. Suitably, these same motor neurons have been shown to be anatomically downstream of the Down-and-Back neuron (A09l)[@Burgos2018], as well as functionally downstream of the mCSIs[@Yoshino2017] - both of which are sufficient to elicit nocifensive behaviour. Silencing the SNa motor neurons (LT-1,2,3,4 motor neurons) with tetanus neurotoxin light chain (TNT) gave no deficit in normal exploratory behaviour (crawling and turning), but did reduce the percentage of animals that performed a roll[@Yoshino2017].

### Longitudinal-linked circuitry

Aside from LT motor neurons Burgos *et al*.[@Burgos2018] identified a complement of premotor neurons downstream of A09l. These PMNs loosely fall into two groups: excitatory neurons innervating lateral transverse muscles or inhibitory neurons innervating longitudinal muscles[@fig:circuitry]. The latter of these groups consists of the A02e and A02g premotor neurons, previously identified by Kohsaka *et al*.[@Kohsaka2014]. This study described A02e and A02g as part of a larger cohort of premotor neuron, termed Period-positive Median Segmental Interneurons (PMSIs), which showed a similar pattern of rhythmic activity to motor neurons, with a short time-delay. Genetic silencing of these neurons increased the duration of a single wave of motor neuron activity and reduced the speed of crawling. This suggested PMSIs are important for regulating the duration of motor neuron bursting and therefore the speed of peristalsis[@Kohsaka2014]. Burgos and colleagues inhibited the entire PMSI population during stimulation of nocifensive behaviour and noted a decrease in the number of rolls performed, but no change to roll bout length or to the percentage of animals that rolled. These results allude to a functional disparity for the PMSI population between nocifensive and basal locomotion.

### Intrasegmental coordination

During rolling behaviour larva maintain a C-shape posture[@Tracey2003]. This left-right asymmetry is presumably instigated and maintained by left-right asymmetric activation of motor cohorts. Heckscher *et al*.[@Heckscher2015] identified a set of 5 premotor neurons expressing the Even-skipped (Eve) transcription factor, Eve Lateral (EL), whose activation (or silencing) caused a asymmetric gait during crawling. Interestingly bilateral muscle activation was still synchronous, but the amplitude of contraction was uncoordinated. TEM tracing of EL neurons revealed direct innervation of MNs for dorsal longitudinal muscles (U1,U2 and RP2, [@fig:muscles]) as well as disynaptic innervation, via the Saaghi-1,3 (SA) premotor neurons, of MNs for predominantly ventral and dorsal longitudinal muscles.

While the EL-Saaghi-MN circuits are a good example of intrasegmental coordination that regulates left-right symmetry, other intrasegmental motifs are required to enforce motor sequencing. To investigate the phase-delay between longitudinal and transverse muscles of a given segment, Zwart *et al*.[@Zwart2016] performed TEM reconstruction of the PMNs upstream of the LT1-4 and LO1 motor neurons ([@fig:muscles]). They identified a single inhibitory GABAergic premotor neuron (iIN-1), projecting exclusively to the lateral transverse MNs, which was capable of producing this phase delay. Silencing iIN-1 resulted in a simultaneous contraction of the longitudinal and transverse muscles[@Zwart 2016]. Interestingly excitatory premotor neurons innervating LT muscles (eIN-1,eIN-2 and eIN-1) and longitudinal muscles (aCC, aka MN1-Ib) are coactive during waves of activity, suggesting iIN-1 is positioned to implement the L-T phase delay.

Undoubtedly intrasegmental circuit motifs are necessary for nocifensive behaviours. However, without the corresponding motor profile, we cannot predict whether these specific premotor circuits are important for C-shape bending or rolling. Despite this, the functional implications of these motifs (phase-delay, left-right synchrony) are likely well conserved and therefore translatable across different behaviours.



## Premotor circuit map

Zarin *et al*.[@Zarin2019a] (published after the work conducted for this thesis) undertook the mammoth effort of reconstructing all 60 MNs and 236 PMNs in a single TEM segment of the larval nervous system. With this they sought to answer how a common population of muscles could generate two distinct behavioural programs, that of forward and backward crawling. Using calcium imaging of patterns of pan-muscle activation they identified differences in the order of muscle recruitment for either behavioural mode. PMN reconstruction did not elucidate specific neurons innervating functionally distinct muscle groups for either behaviour, suggesting combinatorial coding is required to recruit behaviour-specific functional muscle groups. Further, they developed a recurrent network model of PMN and MN neurons across two segments, constrained by the measured connectivity, and demonstrated that the patterns of connectivity in this motor network was sufficient to elicit comparable patterns of muscle contraction for both forward and backward peristalsis. The model was successfully validated on known PMN activity for A14a, A18j, A01c (iIN-1,eIN-1,eIN-2) [@Zwart2016] and A18a[@Hasegawa2016], as well as recordings from novel PMNs (A31k, A06l and A23a)[@Zarin2019a]. This work will prove invaluable for future research, allowing phenotypic and functional studies to be grounded in terms of anatomic connectivity.



# Research Statement

## Rationale

The purpose of this study is to understand how different premotor interneuron populations contribute to the performance of nocifensive behaviours. Further, we hope to assess the relative specificity of said neurons for different behavioural modes and relate this to their anatomical connectivity. We make use of larval *Drosophila melanogaster* for their readily robust and quantifiable behaviours, genetic tractability and relatively small number of neurons. Findings from this research could help in unpicking the neural mechanisms for coordination of distinct locomotor behaviours.



## Aims and hypothesis

**Aim 1:** Identify novel premotor interneuron populations implicated in the performance of nocifensive behaviours in *Drosophila melanogaster* larva. 

**Hypothesis I:** Manipulation of premotor neuron populations necessary for noficensive behaviour will perturb performance of said behaviour. These affects should be quantifiable with metrics describing rolling behaviour as well as posture.

**Hypothesis II:** Established behavioural quantification methods of different design may show discrepancies in scoring nocifensive behaviours. Genotypes presenting robust phenotypic changes should be detectable regardless of the quantitative method used.

​	

**Aim 2:** Characterise the relationship between anatomical connectivity and locomotor involvement across different premotor interneuron populations.

**Hypothesis I:** Manipulation of premotor neurons implicated in nocifensive behaviours will also disrupt basal locomotion.  These affects should be quantifiable with metrics describing crawling and turning behaviours.

**Hypothesis II:** Premotor populations that innervate similar motor neuron cohorts, with the same sign of neurotransmission (excitatory/inhibitory), will be necessary for the performance of similar locomotor patterns.


# Methodology
## Fly strains

**Stocks:**

| Stock      												|
| ---------- |
|*w;;attp2*																	|
|*R72F11-GAL4(attp2)* 														|
|*R69F06-GAL4(attp2)*														|
|*UAS-CsChrimson(attp18);;R72F11-GAL4*										|
|*UAS-CsChrimson(attp18);;R69F06-GAL4*										|
|*UAS-Chrimson::Venus(attp18) (V)*											|
|*72F11-LexA(Jk22),UAS-impTNT-E;13xLexAop-CsChrimson-tdTomato(vk5)*			|
|*72F11-LexA(Jk22),UAS-cTNT-E;13xLexAop-CsChrimson-tdTomato(vk5)*			|
|*72F11-LexA p65(Jk22);13xLexAop-CsChrimson-tdTomato(vk5),UAS-EGFP-Kir2.1*	|
|*w+;UAS-TNTe*																|
|*w;;UAS-Kir2.1-GFP (V)*													|



## Behavioural apparatus

We employed a custom rig for conducting behavioural experiments, of similar design to that in previous publications[@Ohyama2013,@Ohyama2015]. The stage was illuminated by infrared light and recorded by a top-mounted camera. LED under-lighting (624nm) was used for optogenetic stimulation. Recordings were controlled through the Multi-worm Tracker (MWT) software [http://sourceforge.net/projects/mwt](http://sourceforge.net/projects/mwt) [@Swierczek2011] whilst control of the hardware module was controlled through the Stimulus Control Module (SCM) software. Objects detected in MWT are saved as contours from which simple features can be extracted (crabspeed, curve, midline) using the LARA software package [https://sourceforge.net/projects/salam-hhmi/](https://sourceforge.net/projects/salam-hhmi/). 



## Behavioural experiments

Embryos were collected for 24 hours at 25&deg;C. Foraging third instar larvae were used for all experiments. Larvae were raised in the dark at 25&deg;C for 3-4 days on fly food containing *trans*-retinal (Sigma, R2500) at a concentration of 500M.

Before the experiments the larvae were separated from food by suspension in 15% sucrose and with water. Larvae were dried then transferred to the centre of a 25x25 cm transparent plastic, square plate covered in a layer of 2% agar gel. Up to 80 larva were transferred to the plate for any given recording. When using strains containing *UAS-CsChrimson* larval collection and experiments were run in darkness. 



## Behavioural analysis
### Choreography

Behavioural recordings were captured with the Multi-worm Tracker (MWT) software [http://sourceforge.net/projects/mwt](http://sourceforge.net/projects/mwt) [@Swierczek2011]. Raw videos were never saved, due to their large file size. Instead MWT outputs text files with the spine and contour for each object tracked at a refresh rate of approximately 30fps. Objects that were tracked for fewer than 5 seconds, or travelled less than one body length in distance were rejected. From this tracking data we were able to compute key parameters of larval motion using the Choreography program (packaged with MWT)[@Swierczek2011], including generating the spine of the object, curve, speed and crabspeed.



### LARA/Salam/Feature Extraction

To detect the performance of discrete rolling and crawling events we used the LARA software package [https://sourceforge.net/projects/salam-hhmi/](https://sourceforge.net/projects/salam-hhmi/) [@Ohyama2013]. LARA takes, as its input, variables generated by Choreography (described above), using crabspeed for detection of rolling and speed for determining bouts of peristaltic crawling. In brief, detection of a rolling event is determined by the crabspeed value passing a set upper threshold (2.8mm/s) and persists until it drops below a lower threshold (1.8mm/s). Events are combined if they occur within 1 second of one another. A crawling run is defined as a minimum of three consecutive peaks in the speed variable, all of which must exceed a fixed threshold of 0.6mm/s, as well as exceeding 3/10 of the mean peak amplitude computed across the full duration the animal was tracked. A crawling run was broken if the gap between two consecutive good peaks was greater than 2s, or if other behaviours were detected. 



### JAABA

An alternative roll classifier was trained using the "Janelia Automatic Animal Behavior Annotator" (JAABA)[@Kabra2013]. Outline and spine files, generated with Choreography, are input to into JAABA, which are displayed in the GUI. Manual labelling of rolling events allows for supervised training of a behaviour classifier. Training is iterative, allowing the user to score the predicitions made by JAABA, affirming correct prediction and overruling false positives before retraining. The finalised classifier can be applied to other experiments to score behaviour.

Using spine and outline data JAABA computes a suite of 'per-frame' features describing the locomotion, landmarks and appearance of the animal. On top of this, JAABA computes a collection of 'window' features that describe the distribution of per-frame features around the current frame, adding temporal context. The combination of per-frame and window features are then implemented in a 'Gentle Adaboost' learning algorithm [@Friedman2000].




### JBM

A final pipeline[@Jovanic2017], here referred to as the 'JBM', was used to quantify rolling behaviour. Similarly JBM takes, as its input, contour and spine files generated by Choreography. A collection of different features are generated from this describing the locomotion, posture and landmarks of the larvae, which are used to train the classifier. The architecture used to build this supervised learning algorithm consists of an initial Random Forest classifier, a layer to eliminate inconsistencies and a final Random Forest classification layer. This architecture was used to train classification of 6 behaviours[@Jovanic2017] including crawling and rolling.



### Manual Scoring

Insert section on manual scoring




## Statistical analysis

Statistical analyses were performed using customs scripts written with MATLAB (MathWorks) software. Where pairwise comparisons were performed with categorical values (e.g. did roll vs did not roll) the Fishers Exact test was conducted and p values adjusted with the Bonferroni correction. Confidence intervals were calculated as,

$$
CI = p \pm 1.96\times\sqrt{\frac{p(1-p)}{N}}
$$
where *p* is the proportion successful outcomes (did roll). The effect size was calculated using the Odds Ratio, built into the *fishertest* function in MATLAB (2019b).

Where pairwise comparisons were performed with continuous data (e.g. roll percentage, curvature in degrees) we conducted the Wilcoxon rank rum test (Mann-Whitney U test) and adjusted p values with the Bonferroni correction. If all possible comparisons were assessed we instead performed the Kruskal-Wallis test and adjusted p values with the Dunn-Sidak correction. In either case, confidence intervals were defined as the order statistics, *Y~i~* and *Y~j~*, between which the binomial c.d.f equals,


$$
.95 \approx P(Y_i < m < Y_j) \approx\sum^{j-1}_{k=i} \binom{n}{k}(0.5)^k(0.5)^{n-k}
$$
where $j = (n+1)-i$ (outlined [here](https://online.stat.psu.edu/stat414/node/316/)). The effect size was calculated as,
$$
r = \frac{Z}{\sqrt{N_{Obs}}}
$$
using the Z values calculated from the Wilcoxon rank sum test[@Tomczak2014].

For calculations of latency to crabspeed and curve we applied the *findpeaks* function to the frame-to-frame difference for a given metric, stipulating a minimum prominence threshold of 0.4 or 2, respectively. These thresholds were chosen as they were infrequently surpassed in the absence of nocifensive behaviours.




## Immunohistochemistry

The following primary antibodies were used: chicken anti-GFP (1:25, supplier) and rabbit anti-dsRed (1:25, supplier). For secondary antibodies we used Alexa Fluor 488 goat anti-chicken (1:250, supplier) and Alexa Fluor 568 goat anto-rabbit (1:250, supplier).

The protocols used are identical to those listed on the FlyLight website ([https://www.janelia.org/project-team/flylight/protocols](https://www.janelia.org/project-team/flylight/protocols)). The CNS of third instar larvae were dissected in cold 4% phosphate-buffered saline (PBS) then transferred to 4% paraformaldehyde (PFA, supplier) on ice until starting a timed fixation. Samples were fixed in fresh 4% PFA at room tempereature for 1 hour then underwent four 15 minute washes in 0.4% Triton X-100 in PBS (PBT) in PBS. Samples were preblocked with 4% normal goat serum (NGS) for 2 hours at room temperature. Samples were then incubated with primary antibodies in 0.4% PBT for 4 hours at room temperature, then transferred to 4&deg;C for 2 nights. Following four 15 minute washes in 0.4% PBT, the samples were incubated with secondary antibodies in 0.4% PBT for 4 hours at room temperature, then continued incubation at 4&deg;C for two overnights. The samples were washed a final four times for 15 minutes in 0.4% PBT before being mounted in Vectashield mounting medium (supplier). Images were taken with a *Zeiss* Axio Imager fluorescence microscope.





# Results

## Aim 1.1

To elucidate possible candidates for neurons involved in nocifensive rolling behaviour we designed an optogenetic behavioural screen to determine the functional relevance of discrete neuron populations in rolling behaviour. We selected 135 driver lines with expression patters in the ventral nerve cord from the catalogue of split-GAL4 lines maintained by the Fly Light database [@Pfeiffer2010,@Jenett2012,@Li2014]. To test their functional relevance we performed optogenetic co-activation of these neuron populations with Basin neurons [@Ohyama2015] providing two 15 second bouts of red light, with a 30 second interval between bouts. We hypothesised that activation of neuron populations incorporated in the nocifensive circuitry might show changes to the likelihood, amplitude and duration of rolling. 

We compared rolling in the different split-GAL4 lines to a positive control (*attp2;72F11-GAL4,UAS-CsChrimson*) and evaluated rolling based on the metrics generated by the Salam pipeline for scoring behaviour[@Ohyama2013]. For each split-GAL4 line (which we will refer to by the last four digits in their name) tested we achieved 50 < *n* < 250 animals across an average of 4 replications over multiple days. Lines were fewer than 50 animals were tested were ignored. For statistical analysis experiments were only compared to those controls performed on the same-day to account for day-to-day variance. Some figures are normalised by control values, such that the resultant metric is the difference ($\Delta$) between the experimental and same-day control. In order to simplify the discussion of significant results we decided to group lines based on similarities in phenotype across the different metrics analysed.

### Overview of roll analysis

If the neuron populations being tested were important or necessary for rolling behaviour, we expected that we might see a decrease in the incidence of rolling. At an irradiance of 600uW/cm^2^ stimulation reliably induced rolling in 90% of control animals per-trial ([@fig:A1_1]). None of the lines tested showed a significant decrease in roll probability ([@fig:supp_1]). Interestingly, despite the high baseline of roll proportion in controls we did observe several lines that showed an increase in roll proportion. We note that other lines that increase roll proportion may have been occluded, given said high baseline.

![**Interneuron populations modulate escape behaviours across a range of quantifiable metrics.** (**A**) Average proportion of animals per trial that performed at least one roll during stimulation (Fisher's Exact). (**B**) Difference in average time-spent rolling per animal, (**C**) average curvature and (**D**) crabspeed of split-GAL4 lines versus control (Wilcoxon rank sum). Error bars, 95% confidence interval. \* *p* < .05. \** *p* < .01. \*** *p* < .001.](./thesis_aim1_1.svg){#fig:A1_1}



Given the roll proportion was high for most genotypes, to assess changes in the presentation of rolling behaviour we quantified the average time spent rolling per larvae. We observed that 39 of the lines tested showed a significant increase in the time spent rolling, while 5 showed a significant decrease ([@fig:A1_1]). Further we found many lines showed statistically significant increases and decreases in the number of rolls per animal ([@fig:supp1]) and the average amplitude of rolls per animal ([@fig:supp1]), where the amplitude of a roll is defined as the maximum crabspeed during a bout of rolling.

Analysis of roll-specific metrics are limited in that they can only give insight to the specific bouts of time classified as "rolls". As such, lower-level features describing the posture and movement of the larvae can give more general insight into subtler changes in escape behaviour. Of these, high curvature along the "spine" (midline from head to tail) of larvae is indicative of C-bending behaviour, while its co-presentation with increased crabspeed (movement perpendicular to the body axis) is indicative of rolling behaviour. Given that roll bouts are scored determinant on crabspeed (see Methods) it is unsurprising that most of the lines presenting increased roll duration also show increased average crabspeed during stimulation ([@fig:A1_1]C). Notably the change in average curvature of the animals does not co-present with increased rolling, as group 1 showed significantly decreased curvature during the bout of stimulation, while group 2 show a significant increase ([@fig:A1_1]D). 

![**Lines upregulating rolling do so with different posture.** (**A**) Instantaneous percentage of animals rolling, (**B**) average crabspeed and (**C**) curvature of animals in the first phenotypic group. **D**, **E** and **F** show the values of **A**, **B** and **C**, respectively, averaged across the duration of stimulation. (**G**) Instantaneous percentage of animals rolling, (**H**) average crabspeed and (**I**) curvature of animals in the second phenotypic group. **J**, **K** and **L** show the values of **G**, **H** and **I**, respectively, averaged across the duration of stimulation. Orange horizontal bars indicate the bout of optogenetic stimulation. Error bars, 95% confidence interval. \* *p* < 0.05, \** *p* < 0.01, \*** *p* < 0.001.](./thesis_aim1_2.svg){#fig:A1_2}

### Divergent upregulation of escape behaviour

Given an abundance of significant results (likely inflated due to high statistical power, 50 < *n* < 250), we chose to parse our data to find groups of split-GAL4 lines with similar phenotypes. To do this we visualised the aforementioned metrics over the time series of the experiment, allowing us to analyse modulation of escape behaviours at higher temporal resolution. 

Lines presenting with increased roll proportions generally fell into two categories. The first presented with a delayed but increased peak in roll percentage 2 seconds after the onset of stimulation ([@fig:A1_2]A). Roll percentage steadily decreased, yet remained higher than the control, throughout the remainder of stimulation. While *1816* showed a significant increase in crabspeed during stimulation, *p* < 0.001, *r* = .285 ([@fig:A1_2]E), the temporal profile of crabspeed showed only a marginal increase, limited to the first 5 seconds of stimulation ([@fig:A1_2]B). Notably both *1816* and *1817* demonstrated a marked decrease in curve during stimulation, (*1816*) *p* < .001, *r* = .559 and (*1817*) *p* < .001, *r* = .531 ([@fig:A1_2]C,F).

The second group (*0666,1750, 4052, 4232*) showed a strong biphasic response with an initial spike in roll percentage within 1 second of stimulation, followed by a delayed and prolonged increase in roll percentage after ~5 seconds ([@fig:A1_2]G). All of these lines co-presented with and marked increase in crabspeed during the stimulation bout, (*0666*) *p* < .001, *r* = .626, (*1750*) *p* < .001, *r* = .347, (*4052*) *p* < .001, *r* = .642 and (*4232*) *p* < .001, *r* = .607 ([@fig:A1_2]H,K). These lines showed a temporal profile in curve similar to that of the control ([@fig:A1_2]H), though this was significant when averaged across the stimulation bout for *0666*, *p* < .001, *r* = .284 and *4232*, *p* < .001, *r* = .487.

While both of these groups increase the average amount of time larvae spend rolling, the notable differences are the latency of response from group 1, as well as the divergent changes to body curvature between the groups.

### Interneurons reducing performance of escape behaviour

Another group of lines (*1951*, *4245*, *4189*) presented a decrease in roll percentage during the late phase of the stimulation bout ([@fig:A1_3]A), but the average decrease in roll duration across the stimulation bout was only significant for *1951*, *p* = .007, *r* = .347 ([@fig:A1_3]D). This was complemented by a decrease in both the curve and the crabspeed of the larvae throughout the course of stimulation ([@fig:A1_3]B,C,E,F). We note that the percentage of animals rolling for our control data was higher than usual for these particular comparisons, which may have contributed to the significance of these results.

The final line of interest, *4248*, displayed no obvious phenotype for rolling behaviour ([@fig:supp]), but failed to display the stereotyped 'fast-crawl' behaviour that follows a bout of rolling. Typically, following Basin stimulation, larvae show an increase in crawl speed compared to that prior to stimulation (control data, [@fig:A1_3]G). The post-stimulation crawl speed was significantly lower for *4248*, *p* = .003, *r* = .310, compared to the control.

![**Identification of lines that downregulate escape behaviours.** (**A**) Instantaneous percentage of animals rolling, (**B**) average crabspeed and (**C**) curvature of animals in the third phenotypic group. **D**, **E** and **F** show the values of **A**, **B** and **C**, respectively, averaged across the duration of stimulation. (**G**) Average speed for line *4248* across the experiment duration. (**H**) Crawl amplitude after optogenetic stimulation normalised by baseline. Error bars, 95% confidence interval. \* *p* < 0.05, \** *p* < 0.01, \*** *p* < 0.001.](./Thesis_Figure_3.svg){#fig:A1_3}



### Accounting for variability

We were conscious that, as with any behavioural experimentation, there was likely day-to-day variability across our experiments. Specifically we were wary of variation in larval size, as the probability of rolling varies with larval age and, by extension, size (data not shown). As such we restricted experiments to third instar larva and rejected animals with an average area < 2.5mm^2^, below which roll likelihood decreases. 

After implementation of this threshold we did observe differences in the average size of larvae between genotypes ([@fig:supp1]A). These deviations fell in the range of $\pm$ 2 mm^2^. This range was deemed tolerable given the probability of rolling, in most cases, varied by less than $\pm$ 20% ([@fig:supp1]B). 

To determine within-genotype variability we looked at average larval size across different trials for our control data and observed median values from 2.5 to 5mm^2^ ([@fig:supp1]). Interestingly we also saw a large degree of variation in metrics describing rolling behaviours, including per-animal time-spent-rolling ([@fig:supp1]) and average number of rolls ([@fig:supp1]). Whether the variability in these specific metrics is explained by variation in larval size has yet to be determined.

***
## Aim 2.1

Having identified 4 different groups of neurons modulating unique aspects of nocifensive behaviour we choose to focus on the 2 groups showing the strongest phenotypic modulation (group 1 & 2). We selected one line from each group (*1816* & *4232*, respectively) for follow up, as they showed the most consistent phenotypic change on repeated trials. 

*1816* drives expression selectively in a pair of segmentally repeated neurons in the ventral nerve cord (VNC) of the larval nervous system. These neurons have previously been identified as the A02e neurons, part of the family of lineage-related period-positive median segmental interneurons (PMSI) population (includes neurons A02a-k)[@Kohsaka2014]. They are reported to be GABAergic and thus inhibitory interneurons that directly innervate motor neurons[@Kohsaka2019]. *4232* drove expression in an unknown group of approximately 3 pairs of neurons with expression limited to the brain.

### Interneuron phenotypes are robust with different stimulation intensity

The performance of escape behaviour can differ depending on the intensity with which Basin neurons are stimulated. At high intensities rolling behaviours are sustained throughout a period of stimulation, whereas at lower intensities larval switch to crawling behaviours after 5-10s ([@fig:supp]). To determine whether the modulation of escape behaviour by our split lines was consistent at lower stimulus intensities, we repeated our Basin co-activation experiments with an irradiance of 100uW/cm^2^. Consistent with our previous data *1816* and *4232* both showed significant increases in total roll duration (*p* < .001, *r* = .301 and *p* < .001, *r* = .428, respectively) and average crabspeed during stimulation (*p* = .003, *r* = .194 and *p* < .001, *r* = .503, respectively; [@fig:A2_1]), while *1816* also showed a consistent decrease in average curvature, *p* = .007, *r* = .178 ([@fig:A2_1]). 

To test whether this modulation of escape behaviour was bidirectional we inhibited *1816* and *4232* using the tetanus neurotoxin light chain (TNT) whilst applying optogenetic activation of Basin neurons to elicit escape behaviours. We compared these results to a control with no split-GAL4 driven TNT expression (*attp2;Basin>Chrimson*) as well as a within-genotype negative control that expresses an inactive form of TNT (*UAS-impTNT;Basin>Chrimson*). Plotted data were normalised by the attp2 control lines to visualise the within-genotype effect of TNT expression. Silencing *1816* with TNT expression significantly increased roll duration compared to expression of the null TNT construct, *p* < .001, *r* = .280 ([@fig:A2_1]). Likewise, TNT expression increased the average curvature of larvae for *1816*, *p* < .001, *r* = .343, and *4232*, *p* = .005, *r* = .297, when compared to null TNT controls ([@fig:A2_1]). Given that activation versus inhibition of *1816* modulates curvature in opposite directions, the data suggest *1816* may affect bidirectional control on larval curvature during nocifensive behaviour. By contrast, *4232* shows greatest modulation of escape behaviour when activated, and less obvious changes when silenced.



![**1816 and 4232 show bidirectional modulation of nocifensive behaviour.** Images of (**A**) *1816>GFP* and (**B**) *4232>GFP*. (**C-E**) Optogenetic coactivation of Basin neurons and split-GAL4 lines with irradiance 100uW/cm^2^. (**C**) The average total duration of rolls per larvae, (**D**) average crabspeed and (**E**) average curvature of larvae during stimulation. (**F-H**) Optogenetic activation of Basin neurons coupled with silencing (TNT) of split-GAL4 lines. Controlled using a null TNT construct (impTNT). (**F**) The average total duration of rolls per larvae, (**G**) average crabspeed and (**H**) average curvature of larvae during stimulation. Error bars, 95% confidence interval. \* *p* < 0.05, \** *p* < 0.01, \*** *p* < 0.001.](thesis_aim2_1.svg){#fig:A2_1}



### Contribution to basal locomotion

Given both *1816* and *4232* are both implicated in the performance of nocifensive behaviour, we wanted to determine whether they were also necessary for basal locomotor behaviours. First we decided to perform single optogenetic activation of these neurons and assessed metrics associated with crawling (crawl amplitude and frequency) as well as metrics related to normal turning and casting behaviours (average curvature). Activation of *1816* showed no change to either crawl amplitude or frequency but did show a marginal reduction in average curvature during stimulation, *p* = .049, *r* = .129 ([@fig:A2_2]). However *4232* showed significant reduction to both crawl amplitude, *p* < .001, *r*  = .354 ([@fig:A2_2]), and frequency, *p* = .002, *r* = .221 ([@fig:A2_2]), as well as a increase in average curvature, *p* < .001, *r* = .398 ([@fig:A2_2]). 

To complement this experiment we decided to perform single inhibition of these neurons using a TNT construct. TNT silences the neurons permanently, thus no stimulation was required. The most notable result was that silencing *4232* reduces the average curvature of the larvae (*p* < .001, *r* = .348, [@fig:A2_2]), complementing the increase seen with *4232* activation. Referring to the timeseries, we can see that activation of *4232* induces increased curvature throughout the bout of stimulation ([@fig:supp]), though we cannot determine whether this reflects head casting or turning behaviours.

We also observed a small increase in crawl frequency on silencing *1816*, which is consistent with the literature[@Kohsaka2014], *p* = .004, *r* = .264 ([@fig:A2_2]). Together these results suggest that the activity of *4232* affects both posture and peristaltic crawling, whereas *1816* is minimally implicated.



![**4232 modulates body curvature during basal locomotion.** (**A-C**) Single optogenetic activation of  split-GAL4 lines. (**A**) The average crawl amplitude, (**B**) crawl frequnecy and (**C**) curvature of larvae during optogenetic stimulation. (**D-F**) Single silencing of split-GAL4 lines with TNT. (**D**) The average crawl amplitude, (**E**) crawl frequnecy and (**F**) curvature of larvae during free exploration. Error bars, 95% confidence interval. \* *p* < 0.05, \** *p* < 0.01, \*** *p* < 0.001.](thesis_aim2_2.svg){#fig:A2_2}

***

## Aim 2.2

Having identified that A02e modulates the posture of larvae during escape behaviour, but not basal locomotor behaviours, we wanted to identify which motor neurons and muscles are downstream of A02e. This should allow inference into which motor cohorts are specifically important for facilitating these nocifensive behaviours. Further we wanted to assay PMNs affecting similar motor cohorts to determine whether connectomic similarities between PMNs might strengthen predictions of muscles necessary for escape behaviour.  As A02e has been identified as part of the PMSI family we decided to behaviourally characterise different neurons of the A02 lineage. These neurons are morphologically similar[@Kohsaka2014], but the relative differences in their function and connectivity have yet been addressed. 

### A02 connectivity

We searched the [Fly Light Split-GAL4 Driver Collection](https://www.janelia.org/open-science/fly-light-split-gal4-driver-collection)[@Jenett2012] for lines with purported expression in any of the PMSI population and identified lines for A02e (*1816* and *1817*), A02f (*1792*) and A02g (*2175* and *4189*). Imaging the expression of these lines confirmed their selectivity for the aforementioned neurons (data not shown). To determine the connectivity of these neurons we searched for neural reconstructions in a transmission electron microscopy (TEM) volume for an L1 newly hatched larva[@Ohyama2015]. Recent efforts have reconstructed and mapped the synaptic partners of all PMNs and MNs[@Zarin2019a] including those of A02e,f and g ([@fig:A2_3]). A02e makes the majority of its synapses (summarised in [@fig:A2_3]) with motor neurons innervating the VL muscles, specifically MN13 (16 per hemisegment, 24.8% of total output), MN30 (12 per hemisegment, 18.6% of total output) and MN12 (8 per hemisegment, 12.4% of total output).  Similarly, A02g predominantly synapses onto motor neurons innervating VL muscles MN13 (16 per hemisegment, 26.2% of total output), MN30 (17 per hemisegment, 27.9% of total output) and MN12 (4.5 per hemisegment, 7.4% of total output).

However, A02e and A02g differ in that A02e also makes a significant proportion of its outputs to motor neurons innervating DL muscles, like MN4 (5.5 per hemisegment, 8.5% of total output), MN10 (4.5 per hemisegment, 7% of total output), MN3 (4 per hemisegment, 6.2% of total output), whereas A02g forms the remainder of its synapses with motor neurons innervating the VO muscles, like MN15/16 (5 per hemisegment, 8.2% of total output) and MN15/16/17 (6 per hemisegment, 9.8% of total output).

A02f shares most similarities with A02e, innervating MN4 (7.5 per hemisegment, 20.3% of total output) and MN10 (3.5 per hemisegment, 9.5% of total output), both of which project to the DL muscles. However A02f also has unique outputs to the LT projecting motor neurons, MN22/23 (6 per hemisegment, 16.2% of total output) and MN21/22 (2 per hemisegment, 5.4% of total output), as well as the DO projecting motor neuron, MN19 (3.5 per hemisegment, 9.5% of total output).

All 3 neurons also make premotor-to-premotor connections, but those are not reported here.

![**Neurons of the A02 lineage have similar morphology but different connectomics.** Morphology of (**A**) A02e, (**B**) A02f and (**C**) A02g within the first abdominal segment, reconstructed in a TEM volume of the L1 nervous system. (**D**) Number of synapses formed from premotor neuron (y axis) to motor neuron (x axis), as observed in the same TEM volume. Identidy of the muscles anatomically downstream of (**F**) A02e, (**G**) A02f and (**H**) A02g compared to (**E**) reference musculature. Colour indicates the number of (red) contralaterel and (blue) ipsilateral synapses made with the corresponding MN.](thesis_aim2_3.svg){#fig:A2_3}



### A02 modulation of escape behaviour

To test the relative involvement of the different A02 populations in escape behaviour we performed optogenetic co-activation Basin neurons with each of the A02 lines. Given the relative similarity in connectivity between A02e and A02g, we expected these neurons to present the greatest similarity in phenotype.

Consistent with our previous observations, lines expressing A02e showed a delayed peak in the roll percentage ([@fig:A2_4]). We quantified this delay as the "latency to first roll" and found significant increases in latency for lines with expression in A02e (*1816*, *p* < .001, *r* = .326, *1817*, *p* < .001, *r* = .290) and A02f, *p* < .001, *r* = .202, compared to a positive control (*attp2;Basin>Chrimson*; [@fig:A2_4]). Further, to determine whether this delay in roll onset reflected delayed change in postural metrics, we quantified the latency to crabspeed and latency to curve (defined as the time between stimulus onset and rise in respective metric). Latency to crabspeed was significantly increased for A02f, *p* < .001, *r* =  .291, and for both A02e lines, *1816*, *p* < .001, *r* = .523 and *1817*, *p* < .001, *r* = .475 ([@fig:A2_4]). All 3 neurons showed an increase in latency to curve, but this effect was greatest for A02e (*1816*, *p* < .001, *r* = .648 and *1817*, *p* < .001, *r* = .660; [@fig:A2_4]).

All A02 lines demonstrated significant reductions in average curvature and crabspeed during the bout of optogenetic stimulation ([@fig:A2_4]). Interesting, both lines for A02e showed a significant decrease in total roll duration (*1816*, *p* < .001, *r* = .277 and *1817*, *p* = .029, *r* = .148; [@fig:A2_4]). We note that this is different from the result in our original screen and likely reflects changes in the performance of the positive control. 

These results suggest that all the A02 neurons tested are implicated in the performance of escape behaviours, but that A02e and A02f modulate the most similar aspects of behaviour. Specifically, activation of A02e and A02f interferes with the onset of escape behaviours. 




![**A02 neurons differentially modulate escape behaviour.** Optogenetic co-activation of Basin neurons with different A02 neurons. Instaneous roll proportion for (**A**) A02e, (**B**) A02f and (**C**) A02g. (**D**) Average latency to the first bout of rolling. Average latency to initial rise in (**F**) crabspeed and (**H**) curve. (**E**) The average total duration of rolls per larvae, (**G**) average crabspeed and (**I**) average curvature of larvae during stimulation. Error bars, 95% confidence interval. \* *p* < 0.05, \** *p* < 0.01, \*** *p* < 0.001.](thesis_aim2_4.svg){#fig:A2_4}



### A02 modulation of basal locomotion

Given that all A02 neurons tested impacted postural metrics, we tested their function in basal locomotion. To do this we performed both single optogenetic activation and single inhibition (TNT) of the A02 neurons. All lines trend toward an increase in crawl frequency ([@fig:A2_5]) when activated, which was mirrored by a general decrease in crawl frequency when silenced ([@fig:A2_5]). Of these, lines with expression in A02e neurons showed the greatest magnitude of change. These results are consistent with previous literature implicating the A02 population in regulating peristaltic frequency[@Kohsaka2014], however this is one of few studies to test A02 neurons individually[@Kohsaka2019]. Unsurprisingly, genotypes showing a decrease in crawl frequency also showed a decrease in crawl amplitude.

Notably, activation of A02f caused a large and significant increase in curvature during stimulation, *p* < .001, *r* = .495 ([@fig:A2_5]). Specifically, activation of A02f induces a decrease in the percentage of animals crawling, followed by an increase in curvature 5 seconds after the onset of stimulation ([@fig:supp]). Similarly, activation of *4189* (A02g) also induces a significant increase in curvature, *p* < .001, *r* = .211, but with relatively small magnitude.

We also observed significant decreases in average curvature for *1792* (A02f), *p* = .016, *r* = .138, *1817* (A02e), *p* < .001, *r* = .217, and *4189* (A02g), *p* < .001, *r* = .186, but the magnitude of these changes were also negligible. 

These results suggest that none of the neurons in questions are necessary for the performance of crawling behaviour, but that A02f may induce curved posture. Whether this reflects normal head casting behaviour or change of direction is unclear from these analyses. 

![**A02 neurons differentially modulate body posture.** (**A-C**) Single optogenetic activation of A02 neurons. (**A**) The average crawl amplitude, (**B**) crawl frequnecy and (**C**) curvature of larvae during optogenetic stimulation. (**D-F**) Single silencing of A02 neurons with TNT. (**D**) The average crawl amplitude, (**E**) crawl frequnecy and (**F**) curvature of larvae during free exploration. Error bars, 95% confidence interval. \* *p* < 0.05, \** *p* < 0.01, \*** *p* < 0.001.](thesis_aim2_5.svg){#fig:A2_5}



***

## Aim 1.2

Throughout the literature there are numerous methods which implement different algorithms for the detection of discrete behaviours, like rolling. The extent to which these pipelines reach consensus in the scoring of like-named behaviours is unknown. We wanted to assess whether the phenotypic differences observed for rolling behaviour with A02e, originally scored using the Salam pipeline, are consistently identifiable across 2 other common behavioural pipelines (JB and JAABA).

### A02e phenotype is detectable regardless of analytical method

We first set up both the JB pipeline[@Jovanic2020] (with assistance from the [Masson lab](https://research.pasteur.fr/en/team/decision-and-bayesian-computation/)) and JAABA pipelines in the lab. While the JB pipeline already has a trained classifier for detection of rolling behaviour, we had to train a novel classifier for rolling behaviour with the JAABA pipeline (Shua Noh, unpublished). We processed our optogenetic co-activation experiments for A02e and the positive control (*1816,Basin>Chrimson* and *Basin>Chrimson*, respectively) with each of the different classification methods. 

The three pipelines showed visible differences in the scoring of roll behaviours for our control data, which serves as our baseline for quantification of escape behaviour. Salam shows the most conservative scoring of rolling behaviour per larvae, whereas JAABA scores with the greatest abundance ([@fig:A1_4]). When scoring co-activation with A02e, both the JB and JAABA pipelines show are large decrease in the percentage of animals rolling ([@fig:A1_4]). Notably, all pipelines showed an increase in the latency to roll. This suggests that the phenotype originally detected with our pipeline is consistent and robust, rather than a artefact from our choice in method.

![**Performance of different pipelines in scoring rolling behaviour.** (**A-C**) Optogenetic activation of Basin neurons (*Basin > Chrimson*). Ethogram indicating bouts of rolling behaviour as scored by the (**A**) Salam, (**B**) JB and (**C**) JAABA pipelines, apposed to bouts of crawling as scored by Salam. (**D-F**) Optogenetic co-activation of Basin neurons with A02e (*1816*) or a positive control (*attp2*). Instantaneous roll proportion as scored by the (**D**) Salam, (**E**) JB and (**F**) JAABA pipelines. (**G**) The proportion of overlap for classified rolling behaviours, by pipeline, against ground truth scoring for C-bending, rolling or both (roll & C-bend combined). (**E**) The average duration of false positive rolls scored per larvae for each of the pipelines, as compared against ground truth scoring for rolling or escape behaviour generally (roll & C-bend combined).](./thesis_aim1_4.svg){#fig:A1_4}



### Pipelines vary in accuracy and specificity of scoring

Given the magnitude of difference in the scoring of rolling between pipelines we asked what the relative accuracy and specificity in scoring was between these pipelines. To assess this we scored 1 timestamp, consisting of 33 larvae, for two different aspects of escape behaviour. We scored both C-bending behaviour (initiation/maintenance of C-shape posture) against rolling behaviour (C-shape posture coincident with lateral movement) as mutually exclusive behaviours. Distinguishing these two behaviours allowed us to evaluate the specificity of either pipeline for rolling versus escape behaviours more generally.

We quantified the performance of the pipelines by their percentage overlap with the ground truth, as well as the duration of false positives scored. Salam demonstrated the lowest specificity for rolling, labelling 24% of true rolls and 26% of true C-bends. The JB pipeline showed the greatest specificity for scoring rolling, labelling 56% of true rolls compared to just 15% of true C-bends. JAABA also showed improved specificity versus Salam, labelling 87% of true rolls and only 41% of true C-bends.

In assessing false positives, it is important to note that falsely detected "rolls" frequently overlap with true C-bend behaviours. As such, we can assess false positives against rolls separately to false positives against nocifensive behaviours more generally (combination of roll & C-bend). The JB pipeline demonstrates the greatest accuracy, scoring the fewest false positives for either rolling (.59 seconds per larvae) or nocifensive behaviour generally  (.17 seconds per larvae). Salam and JAABA performed with similar accuracy, scoring false positive rolls at 1.39 and 1.86 seconds per larvae, respectively. Both showed greater accuracy when scoring against nocifensive behaviour in general, both scoring fewer than .85 seconds per larvae of false positive behaviour.

These results argue that JB offers best trade off for specificity and accuracy against proportion of behaviours detected. Otherwise JAABA offers the greatest absolute scoring of rolling, but at the cost of some specificity and accuracy.

***

# Bibliography

\singlespacing

<div id="refs"></div>

\doublespacing

# Supplemental

\setcounter{figure}{0} 
\renewcommand{\thefigure}{S\arabic{figure}}




![**Relates to Figure 1.** (**A**) Difference in average area of larvae versus control. (**B**) Difference in average number and (**C**) amplitude of rolls versus control. (**D**) Average  area (mm^2^), (**E**) number of rolls performed and (**F**) time-spent rolling across all each trial for control data. Error bars, 95% confidence interval. \* *p* < 0.05, \** *p* < 0.01, \*** *p* < 0.001.](./thesis_supp2.svg){#fig:supp1}



