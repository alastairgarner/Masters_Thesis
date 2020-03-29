---
# Front matter
title:  "Identification of neural premotor substrates affecting nocifensive behaviour in Drosophila larvae"
author: |
	| Alastair Garner 
	| Supervisor: Dr. Tomoko Ohyama
	| Integrated Program in Neuroscience
date: | 
	| McGill University, Montreal
	| March 2020
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

**Hypothesis 1.1:** Manipulation of premotor neuron populations necessary for noficensive behaviour will perturb performance of said behaviour. These affects should be quantifiable with metrics describing rolling behaviour as well as posture.

**Hypothesis 1.2:** Established behavioural quantification methods of different design may show discrepencies in scoring nocifensive behaviours. Genotypes presenting robust phenotypic changes should be detectable regardless of the quantitative method used.

​	

**Aim 2:** Characterise the relationship between anatomical connectivity and locomotor involvement across different premotor interneuron populations.

**Hypothesis 2.1:** Manipulation of premotor neurons implicated in nocifensive behaviours will also disrupt basal locomotion.  These affects should be quantifiable with metrics describing crawling and turning behaviours.

**Hypothesis 2.2:** Premotor populations that innervate similar motor neuron cohorts, with the same sign of neurotransmission (excitatory/inhibitory), will be necessary for the performance of similar locomotor patterns.


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



## Statistical analysis

Statistical analyses were performed using customs scripts written with MATLAB (MathWorks) software. For our initial screen, the proportions of animals that performed a behaviour (roll) were compared between genotypes using the Fisher's Exact test. Comparison of other metrics were conducted using the Wilcoxon rank sum test (Mann Whitney U test). We only compared control and experimental data from overlapping experimental days to account for day-to-day variance, as well as to limit the power (*n*) of the control data. Where pairwise multiple comparisons were made, for either Fisher's Exact test or Wilcoxon rank rum test, *p* values were corrected using the Bonferroni correction (135 comparisons for screen data).




## Immunohistochemistry

The following primary antibodies were used: chicken anti-GFP (1:25, supplier) and rabbit anti-dsRed (1:25, supplier). For secondary antibodies we used Alexa Fluor 488 goat anti-chicken (1:250, supplier) and Alexa Fluor 568 goat anto-rabbit (1:250, supplier).

The protocols used are identical to those listed on the FlyLight website ([https://www.janelia.org/project-team/flylight/protocols](https://www.janelia.org/project-team/flylight/protocols)). The CNS of third instar larvae were dissected in cold 4% phosphate-buffered saline (PBS) then transferred to 4% paraformaldehyde (PFA, supplier) on ice until starting a timed fixation. Samples were fixed in fresh 4% PFA at room tempereature for 1 hour then underwent four 15 minute washes in 0.4% Triton X-100 in PBS (PBT) in PBS. Samples were preblocked with 4% normal goat serum (NGS) for 2 hours at room temperature. Samples were then incubated with primary antibodies in 0.4% PBT for 4 hours at room temperature, then transferred to 4&deg;C for 2 nights. Following four 15 minute washes in 0.4% PBT, the samples were incubated with secondary antibodies in 0.4% PBT for 4 hours at room temperature, then continued incubation at 4&deg;C for two overnights. The samples were washed a final four times for 15 minutes in 0.4% PBT before being mounted in Vectashield mounting medium (supplier). Images were taken with a *Zeiss* Axio Imager fluorescence microscope.





# Results

## Aim 1

To elucidate possible candidates for neurons involved in nocifensive rolling behaviour we designed an optogenetic behavioural screen to determine the functional relevance of discrete neuron populations in rolling behaviour. We selected 135 driver lines with expression patters in the ventral nerve cord from the catalogue of split-GAL4 lines maintained by the Fly Light database [@Pfeiffer2010,@Jenett2012,@Li2014]. To test their functional relevance we performed optogenetic co-activation of these neuron populations with Basin neurons [@Ohyama2015] providing two 15 second bouts of red light, with a 30 second interval between bouts. We hypothesised that activation of neuron populations incorporated in the nocifensive circuitry might show changes to the likelihood, amplitude and duration of rolling. 

We compared rolling in the different split-GAL4 lines to a positive control (*attp2;72F11-GAL4,UAS-CsChrimson*) and evaluated rolling based on the metrics generated by the Salam pipeline for scoring behaviour[@Ohyama2013]. For each split-GAL4 line (which we will refer to by the last four digits in their name) tested we achieved 50 < *n* < 250 animals across an average of 4 replications over multiple days. For statistical analysis experiments were only compared to those controls performed on the same-day to account for day-to-day variance. Some figures are normalised by control values, such that the resultant metric is the difference ($\Delta$) between the experimental and same-day control. In presenting data from the screen, lines of particular interest will be highlighted across figures for easier identification. These genotypes are grouped by similar phenotype.

### Overview of roll analysis

At an irradiance of 600uW/cm<sup>2</sup> stimulation reliably induced rolling in 90% of control animals per-trial ([@fig:screen_control]A). If the neuron populations being tested were important or necessary for rolling behaviour, we expected that we might see a decrease in the incidence of rolling. Only one line tested gave a significant decrease in the proportion of animals that performed rolling behaviour (*4169*), when compared to the same-day control ([@fig:supp_1]A). Interestingly, despite the high baseline of roll proportion in controls we did observe several lines that showed an increase in roll proportion. We note that other lines that increase roll proportion may have been occluded, given said high baseline.

![**Presentation of rolling varies by genotype and day.** (**A**) Average proportion of animals per trial that performed at least one roll during stimulation (Fisher's Exact). (**B**) Difference in average time-spent rolling per animal versus same-day control (Wilcoxon rank sum). (**C**) Average  area (mm<sup>2</sup>), (D) number of rolls performed and (E) time-spent rolling across all trials for control data. (F) An ethogram displaying the presentation of rolling and crawling behaviours, where the stimulation bout is marked by the orange horizontal bar. Error bars, s.e.m (**A**) or i.q.r (**B**,**C**,**D**,**E**,). \* *P* < 0.05](./Thesis_Figure_1.svg){#fig:screen_control}

We analysed the performance of control animals across each trial to determine day-to-day variability. The likelihood of rolling varies with larval age and, by extension, larval size (data not shown). As such we restricted experiments to third instar larva and rejected animals with an average area < 2.5mm<sup>2</sup>, below which roll likelihood decreases. We saw a range of larval size across our control experiments, with median values from 2.5 to 5mm<sup>2</sup> ([@fig:screen_control]C). Likewise we observed a large degree of variation in the the per-animal time-spent-rolling ([@fig:screen_control]E) and number of rolls between trials ([@fig:screen_control]D). Such variation may confound statistical analyses versus our experimental lines. 

To assess changes in the presentation of rolling behaviour we analysed the average time spent rolling by individual. We observed that 56 of the lines tested showed a significant increase in the time spent rolling, while 3 showed a significant decrease ([@fig:screen_control]B). Further we found many lines showed statistically significant increases and decreases in the number of rolls per animal ([@fig:supp_1]B) and the average amplitude of rolls per animal ([@fig:supp_1]C), where the amplitude of a roll is defined as the maximum crabspeed during a bout of rolling. The abundance of significant results should be viewed cautiously, as having values of 50 < *n* < 250 will increase statistical power.

### Interneurons increasing presentation of rolling behaviour

Whilst we observed changes in the number, duration and amplitude of roll bouts understanding how these changes manifest in the posture and movement of the larva requires analysis of lower-level metrics. Rolling behaviour is characterised predominantly by high curvature along the "spine" (midline from head to tail) coincident with elevated crabspeed (movement perpendicular to the body axis). Given that roll bouts are scored determinant on crabspeed (see Methods) it is unsurprising that most of the lines presenting increased roll duration also show increased average crabspeed during stimulation ([@fig:screen_groups12]A). Notably the average curvature of the animals does not copresent with increased rolling, as *1816* and *1817* showed significantly decreased curvature (*P* < 0.005) during the bout of stimulation ([@fig:screen_groups12]B).

![**Lines upregulating rolling do so with different posture.** (**A**) Difference in average curvature and (**B**) crabspeed of split-GAL4 lines versus control.  (**C**) Instantaneous percentage of animals rolling, (**D**) average crabspeed and (**E**) curvature of animals in the first phenotypic group. **F**, **G** and **H** show the same metrics, respectively, for the second phenotypic group. Orange horizontal bars indicate the bout of optogenetic stimulation. Error bars, i.q.r.. \* *P* < 0.05, \** *P* < 0.01, \*** *P* < 0.005](./Thesis_Figure_2.svg){#fig:screen_groups12}

Given the plethora of significant results and the relative variability of our control data it was important to assess changes to rolling at a finer timescale, as well as on an individual basis, before selecting lines to study further. We rejected all lines where either the experimental larva or same-day controls had *n < 50* and sought to eliminate other lines based on uncharacteristic control data.

To do this we visualised the previously mentioned metrics over the time series of the experiment. Lines presenting with increased roll proportions generally fell into two categories. The first presented with a delayed but increased peak in roll percentage 2 seconds after the onset of stimulation ([@fig:screen_groups12]C). Roll percentage steadily decreased, yet remained higher than the control, throughout the remainder of stimulation. While *1816* showed a significant increase in crabspeed during stimulation (*P* < 0.005) the temporal profile of crabspeed showed only a marginal increase, limited to the first 5 seconds of stimulation ([@fig:screen_groups12]D). Otherwise *1816* and *1817* were indistinguishable from the control. However, both *1816* and *1817* did demonstrate a marked decrease in curve during stimulation ([@fig:screen_groups12]E).

The second group (*0666,1750, 4052, 4232*) showed a strong biphasic response with an initial spike in roll percentage within 1 second of stimulation, followed by a delayed and prolonged increase in roll percentage after ~5 seconds ([@fig:screen_groups12]F). For *0666, 4052* and *4232* this was copresented with and marked increase in crabspeed during the stimulation bout ([@fig:screen_groups12]G). All lines showed a temporal profile in curve similar to that of the control ([@fig:screen_groups12]H).

### Interneurons decreasing escape behaviour performance

Another group of lines (*1951*, *4245*, *4189*) presented a decrease in roll percentage during the late phase of the stimulation bout ([@fig:screen_groups34]A). This was complemented by a decrease in both the curve and the crabspeed of the larvae throughout the course of stimulation ([@fig:screen_groups34]B&C). We noted that the control data was higher than usual for these particular comparisons, perhaps distorting the significance of these results. As such we did not follow up on these particular lines.

The final line of interest, *4248*, displayed no obvious phenotype for rolling behaviour ([@fig:screen_groups34]D), but failed to display the stereotyped 'fast-crawl' behaviour that follows a bout of rolling. Analysis of larval speed in control data shows that, at the end of a bout of stimulation, speed increases above the pre-stimulation baseline ([@fig:screen_groups34]E) *(regenerate this plot to show baseline before stim)*. Larval speed in 4248 only increased to that of baseline.

![**Identification of lines that downregulate escape behaviours.** (**A**) Instantaneous percentage of animals rolling, (**B**) average crabspeed and (**E**) curvature of animals in a group presenting decreased roll likelihood. (**D**) Instantaneous percentage of animals rolling and (**E**) perpendicular speed for line *4248* presenting absence of fast-crawl behaviour.](./Thesis_Figure_3.svg){#fig:screen_groups34}

### Increased roll phenotypes are generally robust

Our data suggested that we might have found candidate lines that modulate different components of larval nocifensive behaviour. To test the robustness of these responses we choose to repeat the experiment at a reduced irradiance (100uW/cm<sup>2</sup>). Basin-activated nocifensive behaviours present differently at different stimulation intensity. At high intensities rolling behaviours are sustained throughout a period of stimulation, whereas at lower intensities larval switch to crawling behaviours after 5-10s (supplemental). Therefore we wanted to know whether the observed phenotypic effects were consistent, or unique to the high-power activation. 

Consistent with our original screen *1816* and *1817* showed an increase in the total time-spent rolling ([@fig:screen_LED05]B,E). While *1816* also had a significant decrease in the average curve during stimulation ([@fig:screen_LED05]C), neither *1816* or *1817* appeared markedly different over the time series of stimulation ([@fig:screen_LED05]F). *1750* and *4232* also showed consist results with the original screen, demonstrating an increase in roll duration and crabspeed across the bout of stimulation ([@fig:screen_LED05]G,H). In contrast to the initial screen *4052* and *0666* did not present an increase in either roll percentage or crabspeed ([@fig:screen_LED05]I,J). Again we note that there is a large variation in the performance of control data, most evidently between the controls run with *4232* and *1750* versus *0666* and *4052*, with an 8-fold increase in the maximum roll percentage ([@fig:screen_LED05]G,I) and 2-fold increase in average crabspeed ([@fig:screen_LED05]H,J). Further repeats will be necessary to determine the validity of these results.

![**Phenotype consistency is varied with reduced stimulation intensity.** (**A**) Average proportion of animals per trial that performed at least one roll during stimulation (Fisher's Exact). (**B**) Difference in average time-spent rolling, (**C**) difference in average curvature and (**D**) difference in average cravspeed versus same-day control (Wilcoxon rank sum).  (**E**) Instantaneous percentage of animals rolling and (**F**) average curvature of for lines *1816* and *1817*.  (**G**) Instantaneous percentage of animals rolling and (**H**) average crabspeed of for lines *1750* and *4232*.  **I** and **J** show the same metrics as **G** and **H**, respectively, for lines *0666* and *4052*. Error bars, s.e.m (**A**) or i.q.r. (**B**,**C**,**D**). \* *P* < 0.05, \** *P* < 0.01, \*** *P* < 0.005.](./Thesis_Figure_4.svg){#fig:screen_LED05}



# Conclusion

Investigation of the neural substrates for motor coordination has been well established for basal locomotion in *Drosophila* larva[@Heckscher2012,@Clark2018a,@Kohsaka2017]. However, how common musculature can be coordinated for the performance of biomechanically dissimilar behaviours is poorly understood. In the case of the larval nocifensive repertoire only a few premotor or motor neurons have been shown to modulate performance of the behaviour[@Yoshino2017,@Burgos2018]. 

The completion of this study should elucidate novel premotor components in the neural circuitry underlying escape behaviours. Further it hopes to address the relative specificity of these premotor components for different behavioural modes. By extension, this could provide insight into the specific muscles necessary for the performance of these behaviours. Together these findings should help in teasing apart the neural mechanisms for coordinating distinct locomotor behaviours.



# Bibliography

\singlespacing

<div id="refs"></div>

\doublespacing

# Supplemental

\setcounter{figure}{0} 
\renewcommand{\thefigure}{S\arabic{figure}}




![**Alternative metrics for split-GAL4 co-activation screen.** (**A**) Difference in proportion of animals per trial that performed at least one roll versus control (Fisher's Exact). (**B**) Difference in average number and (**C**) amplitude of rolls versus control. (**D**) Average curvature and (**E**) crabspeed of animals during stimulation. Error bars, s.e.m (**A**) or i.q.r. (**B**,**C**,**D**,**E**). \* *P* < 0.05, \** *P* < 0.01, \*** *P* < 0.005.](./Supplemental_1.svg){#fig:supp_1}