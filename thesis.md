---
# Front matter
title:  "Identification of neural premotor substrates affecting escape behaviours in Drosophila larvae"
author: Alastair Garner 
date: April 2020
documentclass: article

# Bibliography
link-citations:  true
csl:
	- current-biology.csl
color-links: true
linkcolor: Blue

# Formatting
indent: true
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
	- "Avenir Next"
sansfontoptions:
	- UprightFont = * Regular
	- BoldFont= * Demi Bold
	- ItalicFont= * Italic
	- BoldItalicFont= * Demi Bold Italic
fontsize:
	- 12pt
---

# Abstract {-}

The locomotor repertoire of an individual can encompass a range of distinct motor patterns, all of which are encoded and coordinated by the nervous system. Despite diversity in these behaviours, each locomotor mode is enabled by a limited, common musculature. How neural circuits are organised to facilitate discrete patterns of locomotion is not well understood.

*Drosophila* larvae invoke distinct locomotor patterns for either exploratory or nocifensive behaviours. Here we use optogenetics to perform a high-throughput behavioural screen of ventral nerve cord interneurons for their involvement in the performance of nocifensive behaviour. We identified a set of inhibitory premotor neurons (A02e neurons) which were sufficient to delay the onset of nocifensive behaviour. Behavioural characterisation of the A02e neurons revealed activity-dependent modulation of larval posture during escape behaviours, but not basal locomotor behaviours. Further, A02e-related premotor neurons, which recruit heterogeneous motor cohorts, showed differences in the modulation of both exploratory and nocifensive behaviours.

Our results suggest that certain premotor neurons are differentially recruited between nocifensive and basal behaviours. Based on the neurons assayed we predict that the somatic lateral and dorsal muscles, but not ventral muscles, are particularly important for the initiation of larval escape behaviours. Therefore, whether a premotor neuron is necessary for the performance of a discrete behaviour, depends on the motor cohorts it innervates.

# Résumé {-}

Le répertoire locomoteur d'un individu peut englober une gamme de schémas moteurs distincts, tous codés et coordonnés par le système nerveux. Malgré la diversité de ces comportements, chaque mode locomoteur est activé par une musculature commune limitée. Comment les circuits neuronaux sont organisés pour faciliter des schémas de locomotion discrets n'est pas bien compris.

Les larves de *Drosophila* invoquent des schémas locomoteurs distincts pour les comportements exploratoires ou nocifs. Ici, nous utilisons l'optogénétique pour effectuer un criblage comportemental à haut débit des interneurones du cordon nerveux ventral pour leur implication dans la performance du comportement nocif. Nous avons identifié un ensemble de neurones prémoteurs inhibiteurs (neurones A02e) qui étaient suffisants pour retarder l'apparition d'un comportement nocif. La caractérisation comportementale des neurones A02e a révélé une modulation dépendante de l'activité de la posture larvaire pendant les comportements d'échappement, mais pas les comportements locomoteurs basaux. De plus, les neurones prémoteurs liés à A02e, qui recrutent des cohortes motrices hétérogènes, ont montré des différences dans la modulation des comportements exploratoires et nocifs.

Nos résultats suggèrent que certains neurones prémoteurs sont recrutés de manière différentielle entre les comportements nocifs et basaux. Sur la base des neurones analysés, nous prédisons que les muscles somatiques latéraux et dorsaux, mais pas les muscles ventraux, sont particulièrement importants pour l'initiation de comportements d'échappement larvaires. Par conséquent, le fait qu'un neurone prémoteur soit nécessaire à la réalisation d'un comportement discret dépend des cohortes motrices qu'il innerve.



# Acknowledgements {-}

First, I owe most of my thanks to Dr Tomoko Ohyama, whose kind mentorship and insight has guided me through this degree. I'm truly grateful for the opportunity you've offered me, and am certainly just the first of many students to graduate under your supervision. To Jiayi Zhu, you've been an exceptional lab mate. I immensely appreciate the generosity and assistance you've offered throughout my degree. Thanks to Shua Noh, who offered invaluable discussion for analyses, on top of the thankless task of training numerous behavioural classifiers. I also extend my thanks to the many other students who have passed through the lab. Additional thanks goes to the Moon lab, for use of their microscope.

To Dr. Ed Ruthazer, I cannot thank you enough for the counsel and mentorship throughout my graduate experience. To Dr. Alanna Watt and Dr. Jon Sakata, working with you both offered precious respite from the doldrums of research. I extend my gratitude to my committee members, Dr Michael Hendricks and Dr Brian Chen, who's encouragement and discussion I deeply appreciated. Finally, I would also like to thank Ronan da Silva and Farin Bourojeni, who both demonstrated immense patience, support and friendship during my earliest days in graduate school.

For the beers, I thank Dieu du Ciel and Helm, as well as the father and son who own my local depanneur. For the coffee and the butteriest pastries, my sincere thanks to Brioche à tête and Cafe Saint Louis. And for the copious volume of bagels and bread, my thanks to Guillaume, Fairmount Bagel and Saint Viateur bagel, for I truly have no preference...

A special thanks goes to the entire McElroy family, whose podcasts brought laughter, even during the most monotonous of experiments. A most heartfelt of thanks goes to White Denim, for 4 albums of sweet rockin' rock 'n' roll, in as many years.

I owe tremendous thanks for the holiday pub trips and overwhelming support from my friends back home, to Sam McArdle, Savva Theocharous, Mike Simargool, Will Beedham, Matt Harris, Will Mason, Greg Albery and Jonty Lord. As many thanks again go to Maria Vila de Mucha, for providing much of the emotional support necessary for me to finish this degree. To Lee Rannells, my thanks for being a saint of a housemate, and always being down for board games. And to Izzy Groves and Travis Moore, I cannot show enough appreciation for the countless laughs and happy squash sessions.

To my family, I could write another whole acknowledgements page, for your support permeated every inch of my graduate experience. Your encouragement, advice in the face of uncertainty and offers of some much-needed holiday, all have enabled me to finish this degree. I am incredibly grateful for all of it.

Finally, an immeasurable thank you goes to Kat Cruickshank. For every set-back, there was cake, and for every victory, well... there was also cake. No poor soul should be subjected to that many maggot-related rants, yet you always graciously lent an ear, as well as your support. Thank you, truly.



# Author Contributions {-}

Alastair Garner^a\*^ and Dr. Tomoko Ohyama^b\*^ conceived the project and maintained fly stocks. Alastair Garner performed and analysed all behavioural and imaging experiments. Jiayi Zhu^a^ generated some fly stocks and also offered invaluable discussion. Yassine Rahmouni^a^ and Dr Jean-Baptiste Masson^c,d^ assisted in setting up behavioural pipelines in the lab. Novel behavioural classifiers were trained by Shua Noh^b^. Some fly stocks were generously donated by Dr James W Truman^d^.

The material of this thesis, including all text and figures, were written and produced by Alastair Garner. Edits were offered by Dr Tomoko Ohyama.

\*[alastairgarner@outlook.com](alastairgarner@outlook.com), [tomoko.ohyama@mcgill.ca](tomoko.ohyama@mcgill.ca)



\vfill



\noindent ^a^Integrated Program in Neuroscience, McGill University, Montréal, Canada

\noindent ^b^Department of Biology, McGill University, Montréal, Canada

\noindent ^c^Decision and Bayesian Computation, Neuroscience Department, Institut Pasteur & CNRS, Paris, France

\noindent ^d^Howard Hughes Medical Institute Janelia Research Campus, Ashburn, VA, USA



# Abbreviations {-}

\begin{tabular}{ l l }

DL: & dorsal longitudinal \\

impTNT: & tetanus toxin light chain (inactivated) \\

JAABA: & Janelia Automatic Animal Behavior Annotator \\

JB: & behavioural classification method by Dr. Jean-Baptiste Masson  \\

LT: & lateral transverse \\

MN: & motor neuron \\

PMN: & premotor neuron \\

ssTEM: & single section transmission electron microscopy \\

TEM: & transmission electron microscopy  \\

TNT: & tetanus toxin light chain \\

VL: & ventral longitudinal \\

VNC: & ventral nerve cord \\

VO: & ventral orbital \\

\end{tabular}




# Background
Animals typically present with a number of different locomotor modes that allow them to navigate their environment. These modes can be biomechanically similar, for instance, in forward and backward walking. But across vertebrate and invertebrate species, these can encompass a disparate collection of behaviours, including flying, swimming, crawling and jumping. What distinguishes these behaviours are the discrete spatial and temporal patterns of muscle contraction delineating each locomotor mode. Ultimately, this coordination is facilitated by premotor neurons (PMNs), which recruit specific patterns of motor neurons (MNs), each innervating a specific muscle [@Stifani2014]. Understanding how the nervous system can encode these diverse motor patterns has been a focal point of neuroethological research now for many decades [@Briggman2008].

Multiple architectures can explain how premotor circuitry can facilitate the performance of distinct locomotor patterns. These differ on whether the premotor circuitry, or muscles themselves, show behaviour-specific or multifunctional recruitment across behaviours. For instance, two behaviours may be controlled by two distinct premotor pools, each driving a separate unifunctional muscle group [@Morin2002]. Alternatively, two distinct premotor pools could innervate a single multifunctional muscle group. In this case, muscles are active during both behaviours, but their specific pattern of contraction depends on which of the premotor pools is active [@Ramirez1988]. However, the premotor circuits controlling discrete behaviours aren't necessarily separable. Rather, mutually exclusive behaviours may depend on a common set of PMNs, instead being differentiated by unique spatiotemporal patterns of premotor activity [@Briggman2006;@Bucher2006;@Weimann1991]. In practice, systems implement a combination of these architectures to enable their locomotor repertoire, which has been well established in systems like the leech [@Briggman2006].

While these architectures address mechanisms of motor patterning at the level of local premotor circuitry, evidence suggests that motor coordination requires far more distributed control [Georgopoulos1986;@Kristan1997;@Briggman2008]. As such, it is becoming ever more important to contextualise specific premotor architectures in terms of larger patterns of network activity and connectivity. One model that has emerged as a powerful system in which to address these questions, is the *Drosophila melanogaster* larva. This is, in part, due to the development of techniques for non-invasive neuronal manipulation [@Venken2011], connectomics [@Ohyama2015], population-scale neuronal recording [@Lemon2015] and high-throughput behavioural assay [@Ohyama2013;@Kabra2013;@Vogelstein2014;@Masson2020]. While these tools have been used to characterise components of premotor circuitry necessary for basal crawling behaviours, little is know about the circuitry necessary for alternate behaviours. As such, to address the question of multifunctionality in *Drosophila* PMNs, we aim to identify and characterise novel premotor components of the larval escape behaviour repertoire.



## *Drosophila* as a model system in neuroethology

Use of *Drosophila* as a model system for studying neuroethology originates with the mutagenesis screenings conducted by Seymour Benzer and colleagues, where mutated flies were assayed for novel behavioural phenotypes and behaviour-associated genes determined by genetic mapping [@Konopka1971]. This established the classic "Genes to Behaviour" dogma. The development of the UAS-GAL4 system [@Brand1993] provided a genetic handle for targeted manipulation of specific cell types. This allowed researchers to assay the contribution of restricted cohorts of cell/tissues to individual behaviours. This tool has been advanced with the split-GAL4 system [@Luan2006], with which it is possible to genetically target yet smaller populations of cells - in some cases even a single bilateral pair of neurons. This technique was exploited by Pfeiffer and colleagues [@Pfeiffer2010] and expanded upon by others [@Jenett2012;@Gohl2011;@Li2014b] who, collectively, have generated 1000's of split-GAL4 lines with expression patterns restricted to the fly nervous system. 



Within neuroethology these tools allowed for the manipulation of neuronal activity, with the development of effector lines to silence [@Baines2001;@Paradis2001;@Sweeney1995;@Kitamoto2001] or thermally activate [@Rosenzweig2005;@Rosenzweig2008] neuronal populations of interest. More recently, the advent of optogenetics, in which light activatable ion channels are expressed in neurons of interest, has allowed even greater temporal precision for activating [@Boyden2005] and inhibiting [@Mohammad2017] neurons. With expansion of the catalogue of optogenetic constructs, now including wavelength-shifted variants of channelrhodopsin [@Klapoetke2014], the utility of optogenetics continues to be optimised.



In addition, genetically encoded calcium indicators (GECIs) have been developed to allow imaging of neuronal activity. These constructs, when expressed in a neuron population of interest, allow for visualisation of increases in internal calcium concentration - a proxy for bouts of neuronal activity. In particular *UAS-GCaMP* [@Wang2003], a split flourophore reconstituted by calcium binding, has become widely popular. This construct has since been iterated upon [@Chen2013a;@Dana2019], improving the temporal dynamics, sensitivity and signal-to-noise, allowing for single or population level neural recording with high temporal fidelity.



While much effort focuses on the adult fly, research on *Drosophila* larvae has gained popularity for their reduced behavioural repertoire and comparatively small number of neurons (ca. 10,000 versus 100,000 in the adult). On top of this, larvae have a translucent cuticle, simplifying the application of optogenetics and imaging of neuronal activity. Analytical tools have been adapted from *Caenorhabditis elegans* research [@Swierczek2011] to allow the development of high-throughput behavioural assays in *Drosophila* larvae [@Ohyama2013]. Likewise robust methods for behavioural quantification have also been developed, based on user-curated behavioural definitions [@Ohyama2013], unsupervised hierarchical clustering [@Vogelstein2014] and supervised machine learning techniques [@Kabra2013;@;@Masson2020]. 



## *Drosophila* larval nocifensive behaviour

In their natural environment, *Drosophila* are preyed upon by parasitoid wasps [@Carton1986], like those of the *Chalcidoidea* and *Ichneumonoidea* superfamilies. The female wasp inserts its sharp ovipositior through the larval cuticle and lays an egg. The developing wasp larva then digests the host *Drosophila* from the inside out, eventually resulting in the pupation and eclosion of a juvenile wasp. This predatory behaviour confers a strong selective pressure on *Drosophila* [@Powell1997], which has lead to the evolution of strategies to counter this behaviour. The first of these is a cellular immune response that can destroy the wasp egg, preventing the development of wasp and thus also the death of the *Drosophila* larva [@Rizki1990]. The other is a unique behavioural repertoire in which the *Drosophila* larva produces a stereotyped pattern of nocifensive behaviours. These consist of an initial C-shape bend, where the head and tail are simultaneously moved either to the left or right of the body axis [@Ohyama2013] ([@fig:repertoire]A), followed by a corkscrew-like 'roll' motion, in which the larva rotates around the anteroposterior axis [@Tracey2003] ([@fig:repertoire]B). Although these two locomotor modes may be subsequently repeated, escape behaviours are typically concluded by a bout of 'fast-crawling', where the animal crawls with an elevated frequency of peristalsis ([@fig:repertoire]C). The direction of a roll is dictated by the position at which the wasp ovipositor is inserted, such that the rotation of the larval body removes the ovipositor, preventing egg-laying [@Hwang2007]. 

In laboratory conditions rolling behaviour can be readily elicited by activation of the class IV dendrite arborisation (CIVda or MDIV) neurons [@Grueber2002;@Tracey2003], a class of nociceptive sensory neurons that respond to harsh mechanical stimulation [@Zhong2010], noxious temperatures [@Zhong2012] and strong UV light [@Xiang2010].



![**Escape repertoire of *Drosophila* larvae.** (**A**) C-shape bend involves contraction of the head and tail in the same direction. (**B**) One complete roll represents a full 360 degree rotation around the anteroposterior body axis. (**C**) Fast crawling is biomechanicallly similar to normal crawling but with an increased frequency of peristalsis.](./figures/bend_sequence.svg){#fig:repertoire}



## Neural circuitry for escape behaviour

The class IV dendrite arborization (CIVda or MDIV) neurons are the primary nociceptive neurons in larvae and they tile the larval body wall [@Grueber2002;@Tracey2003]. They were first implicated as nociceptive through identification of the gene *painless* (expressed in CIVda neurons), as mutations of *painless* abolish larval nocifensive responses to thermal or mechanical nociceptive stimuli [@Tracey2003]. The same group later showed CIVda neurons to be both necessary and sufficient for triggering rolling behaviour, by using a complement of neuronal activation and inhibition [@Hwang2007].

A number of papers have begun to elucidate the second-order sensory neurons, downstream of CIVda neurons, that are necessary for escape behaviours. Key to these insights was the generation of a serial section transmission electron microscopy (ssTEM) volume, for the brain of a first instar larva [@Ohyama2015]. This dataset allowed for reconstruction of individual neurons, as well as mapping the number of synaptic connections between pairs of neurons. In total, 14 distinct pairs of neurons have been identified as receiving monosynaptic connections from the CIVda nociceptive neurons [@Gerhard2017]. These postsynaptic partners are conserved between first and third instar larvae [@Gerhard2017]. At present, 7 pairs of these neurons have been shown to elicit escape behaviour when activated, including the Basin (A09a,c) [@Ohyama2015], DnB (A09l) [@Burgos2018], mCSI (A02m/n) [@Yoshino2017], Wave (A02o) [@Takagi2017] and A08n neurons [@Hu2017].

The majority of these escape-sufficient neurons make local projections within the ventral nerve cord (VNC). Of these, 4 pairs of segmentally repeated neurons, termed Basin neurons, receive input from both CIVda and vibration-detecting chordotonal (Ch) neurons [@Ohyama2015]. Imaging these neurons illustrated they were functionally multisensory, and that activation of Ch neurons using a vibration stimulus affected multimodal enhancement of rolling behaviour. Additionally they identified a single neuron pair, termed Goro, that received convergent pathways from Basin neurons, which was also sufficient to elicit rolling behaviour.

Another key target of CIVda neurons are the pair of A09l neurons, coined 'Down-and-Back' (DnB) neurons, which have also been linked to the Goro-mediated roll pathway [@Burgos2018]. Like Basin neurons, A09l neurons are multisensory, receiving monosynaptic input from both CIVda and gentle-touch receptor neurons, CIIda and CIIIda. Ectopic activation of DnB neurons is also sufficient to trigger escape behaviours.

Interestingly, the neurons discovered thus far are differentially implicated in specific elements of the escape repertoire. For instance, activation of Goro triggers C-bending and rolling, but not fast-crawling behaviour [@Ohyama2015]. There is also evidence that C-bending and rolling may be separable, given that the combination of A09l activation and Goro silencing reduces presentation of rolling, but not C-bending [@Burgos2018]. Similarly, SeIN138 (or DP-ilp7) neurons specifically trigger body bending akin to C-bend behaviour, but not rolling [@Hu2017]. How these different behaviours are separably encoded by downstream circuitry is unclear.



![**Neural circuitry underlying nocifensive behaviour.** Neurons highlighted in red are sufficient, when activated, to elicit nocifensive behaviour. The musculature is grouped into transverse (LT) and longitudinal (DL,DO,VL,VO) muscles for simplicity. The downstream partners of Goro, A08n and DP-ilp7 are not known.](./figures/circuit_map.svg){#fig:circuitry}

## Larval musculature

The somatic musculature of *Drosophila* larvae is highly stereotyped and well described [@Bate1990]. Each abdominal hemisegment contains 30 muscles that can broadly be categorised into two groups: the longitudinal muscles, which are arranged in parallel with the body axis, or the transverse muscles, which are circumferential to the body wall [@Bate1990;@Clark2018a] ([@fig:muscles]). Each of these 30 muscles are innervated by a single glutamatergic, excitatory 'big' bouton motor neuron (Ib motor neurons). These MNs are named after the particular muscle they innervate, e.g., MN10 innervates muscle 10 ([@fig:muscles]). In addition, a single 'small' bouton neuron (Is motor neuron) projects to each of the three anatomically related muscle groups - the dorsal longitudinal (DL), ventral longitudinal (VL) and lateral transverse (LT) muscles [@Landgraf2006;@Peron2009a]. 

Given that the Ib-type MNs make one-to-one connections with the somatic muscles, and that they show a lower threshold for recruitment than Is MNs [@Schaefer2010], it is likely that Ib MNs provide the predominant excitatory drive to the muscles. This theory was supported by a live imaging study, which observed that Ib-type activity is closely associated with the contraction of their like-named muscle, during waves of both forward and backward crawling [@Newman2017]. 



![**Larval musculature and motor neurons.** Lateral schematic of the somatic musculature of a single abdominal hemisegment. The muscles are arranged as per the cartoon larva (bottom-right), with the head to the left. The ventral nerve cord (VNC) is coloured dark grey. Each of the somatic muscles is innervated by a single big bouton (Ib) type motor neuron of same name. Common motor neuron pseudonyms are listed apposed to the numerical labels. Muscles are grouped anatomically by their position on the dorsolateral axis and their orientation.](./figures/Thesis_musculature.svg){#fig:muscles}



## Motor cohorts vary by behaviour

The anatomical grouping of muscles also alludes to a potential functional grouping. In fact, functionally co-active cohorts of muscles have previously been identified for crawling behaviours. It has been shown that longitudinal muscles (both ventral and dorsal) contract prior to transverse muscles during posterior to anterior (forward) waves of contraction, based on measurements of muscle length during peristaltic crawling [@Heckscher2012]. This suggested that there is separable premotor circuitry controlling the activity of these different functional muscle cohorts.

A more recent study employed calcium imaging to measure the activation of somatic muscles during forward and reverse crawls [@Zarin2019a]. Interestingly, this demonstrated that different functional groups of muscles are recruited for either behaviour. As such, there must be some degree of unique premotor circuitry, specific for the recruitment of either behavioural mode [@Zarin2019a].

No studies, as of yet, have addressed which cohorts of muscles are active during, or necessary for, nocifensive C-bending or rolling behaviour. However, it seems likely that functionally grouped muscles would be different between basal locomotion and escape behaviours, given their visual biomechanical differences. As such, it will be interesting to determine which premotor neurons are responsible for motor cohort recruitment, and whether these premotor neurons are uniquely implicated in the performance of escape behaviours.



## Motor cohorts for escape behaviours

Both C-bending behaviour and rolling behaviour are distinct from crawling behaviour for displaying asymmetric posture [@Tracey2003]. While the premotor circuitry for escape behaviours has not been widely investigated, some studies have implicated select PMNs, and therefore select motor cohorts, in controlling asymmetric posture. Thus, these PMNs may well be important for nocifensive behaviours. 

One behaviour that demonstrates asymmetric locomotion is self-righting behaviour, in which upside-down larvae must correct its dorsoventral orientation. This behaviour involves left and rightward bending, followed by a 180&deg; rotation - an abridged, but visually similar, behaviour to the full 360&deg;nocifensive roll. A population of LT motor neurons, named for their innervation of the lateral transverse muscles ([@fig:muscles]), were discovered to be necessary for the performance of self-righting [@Picao-Osorio2015]. Silencing these LT neurons impaired the ability of larvae to roll back onto their ventral side. 

The LT neurons were more conclusively implicated in escape behaviours, as silencing of the LT neurons (LT-1,2,3,4, [@fig:muscles]) reduced the percentage of animals that performed a roll [@Yoshino2017]. Notably, these same motor neurons have been shown to be anatomically downstream of the Down-and-Back neuron (A09l) [@Burgos2018], as well as functionally downstream of the mCSIs [@Yoshino2017], both of which are sufficient to elicit nocifensive behaviour. How the activity of these motor neurons contributes to the performance rolling behaviour is not yet known.

Another premotor neuron population associated with left-right asymmetric posture are a set of 5 premotor neurons, which express the Even-skipped (Eve) transcription factor, Eve Lateral (EL) [@Heckscher2015]. Activation or silencing of EL neurons caused an asymmetric gait during crawling. Neural reconstruction of EL neurons in a TEM volume revealed direct excitatory innervation of motor neurons (U1,U2 & RP2) projecting to contralateral DL muscles ([@fig:muscles]). Further, ELs formed disynaptic connections, via the inhibitory Saaghi-1,3 premotor neurons, with motor neurons innervating ipsilateral DL muscles. These results suggested that activation of EL neurons was sufficient to produce asymmetric postures, through asymmetric recruitment of DL muscles. As such, DL muscles may be well suited for the generation of nocifensive C-shaped postures.



## Premotor circuits coordinate motor recruitment 

While premotor neurons recruit spatially specific muscle groups, the performance of behaviour requires the coordinated temporal activation of different motor cohorts. One example of such coordination is the aforementioned phase delay between longitudinal and transverse muscles during forward crawling. The identity of neurons encoding this delay were determined by neural reconstruction in a TEM volume, specifically of PMNs that innervate the LT motor neurons [@Zwart2016] ([@fig:muscles]). They identified a single inhibitory GABAergic premotor neuron, iIN-1, that was exclusively upstream of LT muscles. Silencing iIN-1 abolished the contractile delay between longitudinal and transverse muscle during peristalsis, suggesting that it was sufficient to enforce this temporal muscle recruitment.

Another group of neurons, termed Ifb-Fwd neurons, have been shown to contribute to the antagonism between longitudinal and transverse muscle activation [@Kohsaka2019]. Ifb-Fwd neurons are active during forward waves of peristalsis and make excitatory connections with to two distinct groups of PMNs in the next posterior abdominal segment. The first group provides excitatory innervation of motor neurons projecting to the transverse muscles. The other group affects inhibitory innervation of motor neurons projecting to the longitudinal muscles. This circuit mechanism complements that of iIN-1, as this circuit effectively switches off longitudinal muscle activity during the transverse muscle activation phase [@Kohsaka2019].

Together, these mechanisms use feedforward inhibition and feedback inhibition, respectively, to entrain phase-delay and ensure two antagonistic muscle cohorts are not simultaneously active. While these circuit principles likely also apply for nocifensive behaviour, the identity of the neurons affecting this coordination, as well as the motor cohorts they functionally distinguish, are unknown. 



## The premotor connectome

To understand how distinct behaviours are encoded by the nervous system, those premotor neurons identified as necessary for behaviour need to be contextualised by their anatomic connectivity. Accordingly, a premotor connectome has recently been completed for a single abdominal segment of the larval nervous system, through reconstruction of all 60 MNs and 236 PMNs in a ssTEM volume [@Zarin2019a]. They used this connectome to develop a model network, whose connectivity matched their anatomical data. The model generated patterns of motor activity that were comparable to *in vivo* patterns of muscle contraction, for both forward and backward peristalsis. Further, they showed that the modelled PMNs display temporal patterns of activity that match those recorded in actual larvae, including the previously discussed iIN-1 neuron [@Hasegawa2016]. This data suggests that the organisation of directly premotor circuitry is sufficient to coordinate two different patterns of muscle activation [@Zarin2019a].

One interesting question is whether or not these 236 PMNs are sufficient to coordinate the performance of nocifensive behaviours. However, this dataset cannot answer this question without a corresponding profile of motor or muscle activity for nocifensive behaviour. In lieu of this, we can perform functional assays to implicate premotor populations in the performance of nocifensive behaviours, then refer to their connectivity to hypothesise the functional role of these neurons.



# Research statement

## Rationale

The purpose of this study is to understand how different premotor interneuron populations contribute to the performance of nocifensive behaviours. Further, we hope to assess the relative specificity of said neurons for different behavioural modes and relate this to their anatomical connectivity. We make use of *Drosophila melanogaster* larvae for their robust and readily quantifiable behaviours, genetic tractability and relatively small number of neurons. Findings from this research could help in unpicking the neural mechanisms for coordination of distinct locomotor behaviours.



## Aims and hypothesis

**Aim 1:** Identify novel premotor interneuron populations implicated in the performance of nocifensive behaviours in *Drosophila melanogaster* larva. 

**Hypothesis I:** Manipulation of premotor neuron populations necessary for noficensive behaviour will perturb performance of said behaviour. These affects should be quantifiable with metrics describing rolling behaviour as well as posture.

​	

**Aim 2:** Characterise the relationship between anatomical connectivity and locomotor involvement across different premotor interneuron populations.

**Hypothesis I:** Manipulation of premotor neurons implicated in nocifensive behaviours will also disrupt basal locomotion.  These affects should be quantifiable with metrics describing crawling and turning behaviours.

**Hypothesis II:** Premotor populations that innervate similar motor neuron cohorts, with the same sign of neurotransmission (excitatory/inhibitory), will be necessary for the performance of similar locomotor patterns.

​		

**Aim 3:** Determine the reproducibility of our results with alternative analytical methods.

**Hypothesis I:** Established behavioural quantification methods of different design may show discrepancies in scoring nocifensive behaviours. Genotypes presenting robust phenotypic changes should be detectable regardless of the quantitative method used.




# Methodology
## Fly strains

| Stock    |       						|
| -------------------------------------------------------------- | ---- |
|*w;;attp2* | |
|*SS01816*-GAL4 (A02e)	|[@Pfeiffer2010]	|
|*SS01817-GAL4* (A02e)	|[@Pfeiffer2010]	|
|*SS01792-GAL4* (A02f)	|[@Pfeiffer2010]	|
|*SS02175-GAL4* (A02g)	|[@Pfeiffer2010]	|
|*SS04189*-GAL4 (A02g)	|[@Pfeiffer2010]	|
|*R72F11-GAL4(attp2)* |[@Jenett2012] |
|*R69F06-GAL4(attp2)* |[@Jenett2012] |
|*SS04232-GAL4*	|[@Pfeiffer2010]	|
|*SS00666-GAL4*	|[@Pfeiffer2010]	|
|*SS01750-GAL4*	|[@Pfeiffer2010]	|
|*SS01951-GAL4*	|[@Pfeiffer2010]	|
|*SS04052-GAL4*	|[@Pfeiffer2010]	|
|*SS04245-GAL4*	|[@Pfeiffer2010]	|
|*UAS-CsChrimson(attp18);;R72F11-GAL4* |[@Ohyama2015] |
|*UAS-CsChrimson::Venus(attp18) (V)*|[@Klapoetke2014] |
|*72F11-LexA(Jk22),UAS-impTNT-E;13xLexAop2-CsChrimson-tdTomato(vk5)* | [@Ohyama2015] |
|*72F11-LexA(Jk22),UAS-TNT-E;13xLexAop2-CsChrimson-tdTomato(vk5)* | [@Ohyama2015] |
|*w+;UAS-TNTe* |[@Sweeney1995] |



## Behavioural apparatus

We employed a custom rig for conducting behavioural experiments, of similar design to that in previous publications [@Ohyama2013;@Ohyama2015]. The stage was illuminated by infrared light and recorded by a top-mounted camera (FLIR GS3-U3-51S5M-C camera, 2048x2048 resolution). LED under-lighting (624nm) was used for optogenetic stimulation. Recordings were captured at 30fps and were controlled through the Multi-Worm Tracker (MWT) software ([http://sourceforge.net/projects/mwt](http://sourceforge.net/projects/mwt)) [@Swierczek2011], whilst control of the hardware module was controlled through the Stimulus Control Module (SCM) software (packaged with MWT).



## Behavioural experiments

Embryos were collected for 24 hours at 25&deg;C. Foraging third instar larvae were used for all experiments. Larvae were raised in the dark at 25&deg;C for 3-4 days on fly food containing *trans*-retinal (Sigma, R2500), at a concentration of 500&mu;M.

Before an experiment, larvae were separated from food by suspension in 15% sucrose and then washed with water. Larvae were dried then transferred to the centre of a 25x25 cm transparent plastic, square plate covered in a layer of 2% agar gel. Up to 80 larvae were transferred to the plate for any given recording. When using strains containing *UAS-CsChrimson*, larval collection and experiments were run under IR light. 



## Behavioural analysis
### Choreography

Behavioural recordings were captured with the Multi-worm Tracker (MWT) software [http://sourceforge.net/projects/mwt](http://sourceforge.net/projects/mwt) [@Swierczek2011]. Raw videos were never saved, due to their large file size. Instead MWT outputs text files with the 2D contour (outline) for each object tracked at a refresh rate of approximately 30fps. Objects that were tracked for fewer than 5 seconds, or travelled less than one body length in distance were rejected. Objects with an average area < 2.5mm^2^ were rejected, to exclude larvae younger than third instar stage. From this tracking data we were able to compute key parameters of larval motion using the Choreography program (packaged with MWT) [@Swierczek2011], including the spine, curvature, speed and crabspeed of the object.



### LARA (Salam)

To detect the performance of discrete rolling and crawling events we used the LARA software package ([https://sourceforge.net/projects/salam-hhmi/](https://sourceforge.net/projects/salam-hhmi/)) [@Ohyama2013]. LARA takes, as its input, variables generated by Choreography (described above), using crabspeed for detection of rolling and speed for determining bouts of peristaltic crawling. In brief, a 'roll' event is scored when an object's crabspeed surpasses an upper threshold (2.8mm/s), and persists until it drops below a lower threshold (1.8mm/s). Events are combined if they occur within 1 second of one another. A crawling run is defined as a minimum of three consecutive peaks in the speed variable, all of which must exceed a fixed threshold of 0.6mm/s, as well as exceeding 3/10 of the mean peak amplitude computed across the full duration the animal was tracked. A crawling run was broken if the gap between two consecutive good peaks was greater than 2s, or if other behaviours were detected. 



### JAABA

An alternative roll classifier was trained using the 'Janelia Automatic Animal Behavior Annotator' (JAABA) [@Kabra2013]. Training occurs via supervised learning, thus requires manual labelling of roll events. For said labelling, roll bouts were demarcated as the frames between which larvae presented movement perpendicular to the body axis, coincident with C-shape posture (Shua Noh, unpublished).

Input files to JAABA are the outline and spine files generated from Choreography. From these files JAABA computes a suite of 'per-frame' and window features describing the locomotion, landmarks and appearance of the animal, which are used to train the classifier [@Kabra2013]. A detailed description of the pipeline can be found in Kabra et al., 2013 [@Kabra2013].




### JB

A final pipeline, here referred to as the 'JB', was used to quantify rolling behaviour [@Masson2020]. The JB pipeline comes with pre-trained classifiers for rolling and 5 other larval behaviours. Consistent with other pipelines, contour and spine files generated by Choreography are taken as input. A detailed description of the network and how it was trained can be found in Masson et al., 2020 [@Masson2020].



### Manual Scoring

Manual scoring of escape behaviours was performed on a single timestamp of 33 larvae. Two modes of nocifensive behaviour were scored. C-shape bending was scored as a unilateral contraction of both head and tail in the same direction. These bouts were demarcated from the frame where larvae initiated the unilateral contraction, to the first frame where larvae started to unfurl. A roll was scored when larvae presented C-shape posture coincident with travel > 1 body width perpendicular to the larval body axis. Roll bouts were terminated if larvae started to unfurl or lateral movement stopped.

Where C-shape bending transitioned into a roll, scoring of the C-shape bend was truncated by the first frame of perpendicular movement. Where larvae transitioned from a leftward to a rightward C-shape bend (or vice versa), bouts were appended.



## Cluster analysis

To group genotypes from our original optogenetic screen we performed agglomaterive hierarchical clustering, based on three metrics: curvature, crabspeed and time-spent rolling. First, we calculated the average of each of these metrics for every animal, then took the median value of these for each genotype. Genotypes were standardised relative to the same-day control,

$$
z_{i} = \frac{x_{i} - x_{c}}{\sigma_{p}}
$$
where $z_{i}$ is the z-score for a given genotype, $x_{i}$ is the genotype median, $x_{c}$ is the same-day control median and $\sigma_{p}$ is the standard deviation of the full population of genotypes.

Second, the euclidean distance is calculated for every possible pair of genotypes to form a distance matrix ([*pdist*](https://www.mathworks.com/help/stats/pdist.html) function). The distance matrix is the subject to agglomerative hierarchical clustering ([*linkage*](https://www.mathworks.com/help/stats/linkage.html) function), using the *complete linkage* method, though similar clusters were achieved with the *average linkage* method. Based on the linkages, we chose to split the genotypes into 4 distinct clusters, grounded with the following assumptions:

1. The majority of split-GAL4 lines tested will show little difference in escape performance to the control.
2. More than one phenotype will be detectable, given the range of motions in escape behaviour.
3. Large numbers of clusters will show minimal measurable difference, given the limited number of features (3) used.

To visualise the distances between genotypes and clusters we performed principal component anlysis ([*pca*](https://www.mathworks.com/help/stats/pca.html) function) on the standardised metric values, reducing the data from 3 dimensions to 2.



## Statistical analysis

Statistical analyses were performed using custom scripts written with MATLAB (2020b) [@MATLAB2020]. Code for the generation of figures and statistical analyses will be made available at [https://github.com/alastairgarner/JAABA_featExtract](https://github.com/alastairgarner/JAABA_featExtract).

Pairwise comparisons of categorical values (e.g. did roll vs did not roll) were conducted using the Fishers Exact test and p values adjusted with the Bonferroni correction. Confidence intervals were calculated as,
$$
CI = p \pm 1.96\times\sqrt{\frac{p(1-p)}{N}}
$$
where *p* is the proportion of a successful outcome (did roll). The effect size was calculated using the Odds Ratio, built into the [*fishertest*](https://www.mathworks.com/help/stats/fishertest.html) function in MATLAB.

Where pairwise comparisons were performed with continuous data (e.g. roll percentage, curvature in degrees) we conducted the Wilcoxon rank rum test (Mann-Whitney U test) and adjusted p values with the Bonferroni correction. If all possible comparisons were assessed, we instead performed the Kruskal-Wallis test and adjusted p values with the Dunn-Sidak correction. In either case, confidence intervals were defined as the order statistics, *Y~i~* and *Y~j~*, between which the binomial c.d.f approximates to .95,


$$
.95 \approx P(Y_i < m < Y_j) \approx\sum^{j-1}_{k=i} \binom{n}{k}(0.5)^k(0.5)^{n-k}
$$
where $j = (n+1)-i$ (outlined [here](https://online.stat.psu.edu/stat414/node/316/)). The effect size was calculated as,
$$
r = \frac{Z}{\sqrt{N_{Obs}}}
$$
where $Z$ values were calculated using the Wilcoxon rank sum test and $N_{Obs}$ are the number of observations used in calculating said $Z$ statistic [@Tomczak2014]. Effect sizes were deemed to be small, .1 < *r* < .3, medium, .3 < *r* < .5, or large, .5 < *r*, based on Cohen (1992) [@Cohen1992].

For calculations of latency to crabspeed and curve, we applied the [*findpeaks*](https://www.mathworks.com/help/signal/ref/findpeaks.html) function to the frame-to-frame difference for a given metric, stipulating a minimum prominence threshold of 0.4 or 2, respectively. These thresholds were chosen as they were infrequently surpassed in the absence of nocifensive behaviours.

For analyses and visualisation, we also used the following community-developed packages and toolboxes: perceptually uniform colormaps [@Biguri2020], cbrewer [@Charles2020], plotboxpos [@Kearney2020], violinplot [@Hoffmann2020] and yamlmatlab [@Cigler2011].




## Immunohistochemistry

The following primary antibodies were used: chicken anti-GFP (1:25, Abcam) and rabbit anti-dsRed (1:25, Clontech). For secondary antibodies we used Alexa Fluor 488 goat anti-chicken (1:250, Life Technologies) and Alexa Fluor 568 goat anti-rabbit (1:250, Invitrogen).

The protocols used are identical to those listed on the FlyLight website ([https://www.janelia.org/project-team/flylight/protocols](https://www.janelia.org/project-team/flylight/protocols)). The CNS of third instar larvae were dissected in cold 4% phosphate-buffered saline (PBS) then transferred to 4% paraformaldehyde (PFA) on ice until starting a timed fixation. Samples were fixed in fresh 4% PFA at room tempereature for 1 hour then underwent four 15 minute washes in 0.4% Triton X-100 in PBS (PBT) in PBS. Samples were preblocked with 4% normal goat serum (NGS) for 2 hours at room temperature. Samples were then incubated with primary antibodies in 0.4% PBT for 4 hours at room temperature, then transferred to 4&deg;C for 2 nights. Following four 15 minute washes in 0.4% PBT, the samples were incubated with secondary antibodies in 0.4% PBT for 4 hours at room temperature, then continued incubation at 4&deg;C for two overnights. The samples were washed a final four times for 15 minutes in 0.4% PBT before being mounted in Vectashield mounting medium (Vector Labs). Images were taken with a *Zeiss* Axio Imager fluorescence microscope.



# Results

## Aim 1.1

To elucidate possible candidates for neurons involved in nocifensive rolling behaviour, we designed an optogenetic behavioural screen to determine the functional relevance of discrete neuron populations in rolling behaviour. We selected 135 driver lines with expression patterns in the ventral nerve cord from the catalogue of split-GAL4 lines maintained by the Fly Light database [@Pfeiffer2010;@Jenett2012;@Li2014b]. To test whether the neuron populations labelled by these lines are involved in nocifensive behaviour, we performed optogenetic co-activation of these neurons with Basin neurons [@Ohyama2015], providing two 15 second bouts of red light at an irradiance of 600&mu;W/cm^2^, with a 30 second interval between bouts. These were compared to a driver control, *attp2;Basin>CsChrimson*, which exclusively activates escape behaviours.

For each split-GAL4 line tested (which we will refer to by the last four digits in their name), we achieved 50 < *n* < 250 animals, across an average of 4 replications over multiple days. Lines where fewer than 50 animals were tested, were ignored. For statistical analysis, experiments were only compared to those controls performed on the same-day, to account for day-to-day variance.

![**Split-GAL4 lines can be subdivided into four phenotypically similar clusters.** Co-activation of each split-GAL4 line with Basin neurons. (**A**) Dendrogram representing the hierarchical clustering of genotypes based on the *complete linkage* method. (**B**) Distribution of clusters with respect to the first and second pricipal components. (**C**) Standardised crabspeed, (**D**) curvature and (**E**) time-spent rolling for each genotype within their respective clusters. Data is standardised to the control, *attp2;Basin>CsChrimson*, such that positive or negative deflections represent an increase or decrease, respectively, relative to the control. Black horizontal lines indicate the cluster median, vertical lines indicate the upper and lower quartiles. Black scatter outlines highlight genotypes discussed in the following sections. Stimulation irradiance, 600&mu;W/cm^2^.](./figures/Thesis_Figure_Cluster.svg){#fig:A1_1}

### Identification of phenotypically similar split-GAL4 lines

To directly assess changes to the performance of nocifensive rolling, we quantified discrete bouts of rolling using the Salam pipeline (see Methodology) [@Ohyama2013]. For more indirect measures of escape behaviour we analysed the crabspeed and curvature metrics output from the Choreography package (see Methodology) [@Swierczek2011]. High curvature along the 'spine' (midline from head to tail) of a larvae is indicative of C-bending behaviour, while its co-presentation with increased crabspeed (movement perpendicular to the body axis) is indicative of rolling behaviour.

To elucidate patterns in the escape behaviour modulation we clustered genotypes based on their average crabspeed, curvature and time-spent rolling, across the bout of stimulation. Values were standardised by the same-day control, such that metrics were expressed as standard deviations either side of the control. These standardised values were then subject to agglomerative hierarchical clustering, to determine the linkage (i.e. similarity) between genotypes (see Methodology).

Visualisation of linkages with a dendrogram allowed us to cluster genotypes into 4 distinct groups, with the control data falling into the first of these groups ([@fig:A1_1]A). To understand the phenotypic differences between these groups, we compared the average of the standardised metrics for each group ([@fig:A1_1]C-E). As expected, group 1, which contained our control genotype, showed little deviation around the control value ($y=0$) for each of these metrics. Group 4 was the only group that showed a decrease in all three metrics ([@fig:A1_1]C-E), suggesting an overall decrease in the presentation of escape behaviours. Interestingly, both groups 2 and 3 showed an increase in time-spent rolling ([@fig:A1_1]E), but differed otherwise, as group 2 displayed a decrease in curvature ([@fig:A1_1]D), while group 3 presented with increased crabspeed ([@fig:A1_1]C).



![**Lines upregulating rolling differ by temporal profile.** Co-activation of groups 2 & 3 with Basin neurons with irradiance 600&mu;W/cm^2^. (**A**) Instantaneous percentage of animals rolling, (**B**) average crabspeed and (**C**) curvature of animals in the second phenotypic group. (**D**) Average time spent rolling, per larva. **E** and **F** show the values of **B** and **C**, respectively, averaged across the duration of stimulation. (**G**) Instantaneous percentage of animals rolling, (**H**) average crabspeed and (**I**) curvature of animals in the third phenotypic group. (**J**) Average time spent rolling, per larva. **K** and **L** show the values of **H** and **I**, respectively, averaged across the duration of stimulation. Horizontal orange bar, stimulation bout. Error bars, 95% confidence interval. *n*, indicated in plot. \* *p* < 0.05, \** *p* < 0.01, \*** *p* < 0.001.](./figures/thesis_aim1_2.svg){#fig:A1_2}



### Changes in rolling vary independently of curvature and crabspeed

To better understand the changes to escape behaviour, we visualised the aforementioned metrics over the time series of the experiment compared to same-day controls. For this, we selected a subset of genotypes presenting with a combination of large magnitude of change, consistent phenotype on repeated trials and large $n$ values, for each of our phenotypic groups.

Group 2 lines (*1816*, *1817*) presented with a delayed but increased peak in roll percentage 2 seconds after the onset of stimulation ([@fig:A1_2]A). Roll percentage steadily decreased, yet remained higher than the control, throughout the remainder of stimulation. Of these lines, *1816* showed a significant increase in crabspeed during stimulation, *p* < 0.001, *r* = .285 ([@fig:A1_2]E). However, the temporal profile of crabspeed indicated only a marginal increase, limited to the first 5 seconds of stimulation ([@fig:A1_2]B). Notably both *1816* and *1817* demonstrated a marked decrease in curve during stimulation, (*1816*) *p* < .001, *r* = .559 and (*1817*) *p* < .001, *r* = .531 ([@fig:A1_2]C,F).

The third group (*0666, 1750, 4052, 4232*) showed a strong biphasic response, with an initial spike in roll percentage within 1 second of stimulation, followed by a delayed and prolonged increase in roll percentage after ~5 seconds ([@fig:A1_2]G). All of these lines co-presented with a marked increase in crabspeed during the stimulation bout, (*0666*) *p* < .001, *r* = .626, (*1750*) *p* < .001, *r* = .347, (*4052*) *p* < .001, *r* = .642 and (*4232*) *p* < .001, *r* = .607 ([@fig:A1_2]H,K). These lines showed a temporal profile in curve similar to that of the control ([@fig:A1_2]H), though this was significantly increased when averaged across the stimulation bout for *0666*, *p* < .001, *r* = .284 and *4232*, *p* < .001, *r* = .487.

Thus, increases in roll duration can independently vary with larval curvature or crabspeed. For group 2, the large effect of decreased curvature suggests a potential decrease in the presentation of C-shape bending behaviour. Whereas, a large effect of increased crabspeed for group 3 suggests that either larvae spend more time moving perpendicular to their body axis, or that they do this with a greater amplitude than control animals.



### Interneurons reducing performance of escape behaviour

Our fourth group (*1951*, *4245*, *4189*) presented a decrease in roll percentage during the late phase of the stimulation bout ([@fig:A1_3a]A), which was reflected by a significant decrease in average time spent rolling for line *1951*, *p* = .007, *r* = .347 ([@fig:A1_3a]D). This was complemented by a decrease in both the curve and crabspeed of the larvae throughout the course of stimulation ([@fig:A1_3a]B,C,E,F). We note that, for this particular group, the average time spent rolling in our controls animals was higher than usual, which may have contributed to the significance of these results.

![**Identification of lines that reduce the presentation of escape behaviours.** Co-activation of group 4 with Basin neurons with irradiance 600&mu;W/cm^2^. (**A**) Instantaneous percentage of animals rolling, (**B**) average crabspeed and (**C**) curvature of animals in the fourth phenotypic group. (**D**) Average time-spent rolling per larva. **E** and **F** show the values of **B** and **C**, respectively, averaged across the duration of stimulation. Horizontal orange bar, stimulation bout. Error bars, 95% confidence interval. *n*, indicated in plot. \* *p* < 0.05, \** *p* < 0.01, \*** *p* < 0.001.](./figures/thesis_aim1_3.svg){#fig:A1_3a}



## Aim 2.1

Having identified 3 groups of phenotypes that differed from controls, each modulating unique aspects of nocifensive behaviour, we choose to focus on the 2 groups showing the strongest phenotypic modulation (group 2 & 3). We selected one line from each group (*1816* & *4232*, respectively) for follow up, as they showed the most consistent phenotypic change on repeated trials (data not shown). 

Split-GAL4 line *1816* drives expression selectively in a pair of segmentally repeated neurons in the ventral nerve cord (VNC) of the larval nervous system ([@fig:A2_1]A). These neurons have previously been identified as the A02e neurons, part of a family of lineage-related period-positive median segmental interneurons (PMSI) population, which include neurons A02a-k [@Kohsaka2014]. They are reported to be GABAergic, thus inhibitory, interneurons that directly innervate motor neurons [@Kohsaka2019]. Line *4232* drove expression in an unknown group of approximately 3 pairs of neurons, with expression limited to the brain ([@fig:A2_1]B).

### Nocifensive curvature is inversely related with *1816* activity

The performance of escape behaviour can differ depending on the intensity with which Basin neurons are stimulated. At high intensities, rolling behaviour is most prominent 5-10 seconds after the onset of stimulation, whereas at lower intensities, rolling is most prominent during the first 5 seconds of stimulation ([@fig:supp2]B). Likewise, crawling behaviour is suppressed throughout the period of stimulation with high intensity stimulation, but at lower intensities larval switch escape modality to crawling 5-10s after stimulation onset ([@fig:supp2]A). To determine whether the modulation of escape behaviour by our split lines was consistent at lower stimulus intensities, we repeated our Basin co-activation experiments with an irradiance of 100&mu;W/cm^2^. 

Most results were consistent with the data collected at higher light intensities. Both *1816* and *4232* showed significant increases in total roll duration, *p* < .001, *r* = .301 and *p* < .001, *r* = .428, respectively ([@fig:A2_1]C). Notably, *4232* showed an increase in average crabspeed, *p* < .001, *r* = .503 ([@fig:A2_1]D), while *1816* demonstrated decreased average curvature, *p* = .007, *r* = .178 ([@fig:A2_1]E). Line *1816* did also show an increase in average crabspeed, *p* = .003, *r* = .194, but the magnitude of this change was small ([@fig:A2_1]D). This data affirmed our previous observations that both *1816* and *4232* can affect an increase in roll duration, but that *1816* predominantly affects posture (curve), while *4232* primarily affects crabspeed.

To test whether these neurons are necessary for nocifensive behaviour, we silenced *1816* and *4232* using the tetanus neurotoxin light chain (TNT) [@Sweeney1995;@Kitamoto2001], whilst applying optogenetic activation of Basin neurons to elicit escape behaviours. We compared these results to a driver control with no split-GAL4 driven TNT expression (*attp2>TNT;Basin>CsChrimson*), as well as a within-genotype effector control that expresses an inactive form of TNT (*>impTNT;Basin>CsChrimson*). Graphed data were normalised by their respective driver control to visualise the within-genotype effect of TNT expression. Silencing *1816* with TNT expression significantly increased roll duration compared to expression of the null TNT construct, *p* < .001, *r* = .280 ([@fig:A2_1]F). Likewise, TNT expression increased the average curvature of larvae for *1816*, *p* < .001, *r* = .343, and *4232*, *p* = .005, *r* = .297, when compared to null TNT controls ([@fig:A2_1]H). 

Given that the effect of activating or silencing *1816* modulates curvature in opposite directions, the data suggest that the activity of *1816* has an inverse relationship with larval curvature, during nocifensive behaviour. By contrast, *4232* shows pronounced modulation of rolling and crabspeed when ectopically activated, but its endogenous activity is not necessary for normal presentation of escape behaviours.

![**Line *1816* shows activity-dependent modulation of nocifensive posture.** Images of (**A**) *1816>GFP* and (**B**) *4232>GFP*. (**C-E**) Optogenetic coactivation of Basin neurons and split-GAL4 lines with irradiance 100uW/cm^2^. (**C**) The average total duration of rolls per larvae, (**D**) average crabspeed and (**E**) average curvature of larvae during stimulation. (**F-H**) Optogenetic activation of Basin neurons coupled with silencing (TNT) of split-GAL4 lines with irradiance 600uW/cm^2^. Controlled using a null TNT construct (impTNT). (**F**) The average total duration of rolls per larvae, (**G**) average crabspeed and (**H**) average curvature of larvae during stimulation. Error bars, 95% confidence interval. *n*, indicated in plot. \* *p* < 0.05, \** *p* < 0.01, \*** *p* < 0.001.](./figures/thesis_aim2_1.svg){#fig:A2_1}



### Line *1816* shows behaviour-specific modulation of locomotion

Having demonstrated that ectopic activation of either *1816* or *4232* can modulate the performance of nocifensive behaviours, we wanted to determine whether they were also implicated in basal locomotor behaviour. To test this, we performed optogenetic activation of these neurons and assessed metrics associated with crawling (crawl amplitude and frequency), as well as metrics related to baseline turning and casting behaviours (average curvature). Activation of *1816* showed no change to either crawl amplitude or frequency ([@fig:A2_2]A,B), but did show a marginal reduction in average curvature during stimulation, *p* = .049, *r* = .129 ([@fig:A2_2]C). By contrast, *4232* showed significant reductions to both crawl amplitude, *p* < .001, *r*  = .354 ([@fig:A2_2]A), and frequency, *p* = .002, *r* = .221 ([@fig:A2_2]B), as well as an increase in average curvature, *p* < .001, *r* = .398 ([@fig:A2_2]C, [@fig:supp3]B). In fact, activation of *4232* reduced the number of larvae presenting crawling behaviour ([@fig:supp3]A). 

Together these results suggest that activation of *1816* has little affect on basal crawling and posture, while *4232* activity disrupts crawling behaviours. Whether this reflects an active suppression of crawling circuitry or activation of conflicting motor programs, we cannot yet determine.

To determine whether these neurons are strictly necessary for basal locomotion, we inhibited *1816* and *4232* using a TNT construct. The most notable result was that silencing *4232* reduces the average curvature of the larvae, *p* < .001, *r* = .348 ([@fig:A2_2]F), complementing the increase seen with *4232* activation. We also observed a small increase in crawl frequency on silencing *1816*, which is consistent with the literature [@Kohsaka2014], *p* = .004, *r* = .264 ([@fig:A2_2]E). However the magnitude of this effect was small. 

Our data shows that both of the neurons assayed are differentially implicated in nocifensive and basal locomotor behaviours. While *1816* activity modulates nocifensive curvature, it has little effect on basal locomotion. By contrast, *4232* upregulates curvature during basal locomotion, but upregulates crabspeed and rolling during nocifensive behaviours. As such, locomotor modulation by *1816* is seemingly behaviour-specific, whereas *4232* shows little behaviour specificity.



![**4232 modulates body curvature during basal locomotion.** (**A-C**) Optogenetic activation of  split-GAL4 lines. (**A**) The average crawl amplitude, (**B**) crawl frequnecy and (**C**) curvature of larvae during optogenetic stimulation with irradiance 600&mu;W/cm^2^. (**D-F**) Silencing of split-GAL4 lines with TNT. (**D**) The average crawl amplitude, (**E**) crawl frequnecy and (**F**) curvature of larvae during free exploration. Error bars, 95% confidence interval. *n*, indicated in plot. \* *p* < 0.05, \** *p* < 0.01, \*** *p* < 0.001.](./figures/thesis_aim2_2.svg){#fig:A2_2}



## Aim 2.2

As A02e directly innervates motor neurons, the observed modulation of posture is likely caused by those muscles downstream of A02e. Thus, identification of the MNs and muscles downstream of A02e should allow inference as to which motor cohorts might facilitate nocifensive behaviours. If these motor cohorts are indeed important for the performance of escape behaviours, then PMNs recruiting the same motor cohorts should affect a similar modulation of behaviour. To test these hypotheses, we sought to behaviourally assay PMNs upstream of different motor cohorts. We decided to focus on the PMSI family of neurons, a group of lineage-related and inhibitory PMNs, which includes A02e [@Kohsaka2014]. These neurons are morphologically similar, but the relative differences in their function and connectivity have yet been described. 

### A02 neurons are upstream of different motor cohorts

We searched the [Fly Light Split-GAL4 Driver Collection](https://www.janelia.org/open-science/fly-light-split-gal4-driver-collection) [@Jenett2012] for lines with purported expression in any of the PMSI population, and identified lines for A02e (*1816* and *1817*), A02f (*1792*) and A02g (*2175* and *4189*). Imaging the expression of these lines confirmed their selectivity for the aforementioned neurons (data not shown). To determine the connectivity of these neurons, we searched for neural reconstructions in a transmission electron microscopy (TEM) volume for an L1 newly hatched larva [@Ohyama2015]. Recent efforts have reconstructed and mapped the synaptic partners of all PMNs and MNs [@Zarin2019a], including those of A02e, f and g. All three neurons form their synaptic partners within the same abdominal segment ([@fig:A2_3a]A,B,C, respectively). Further, their postsynaptic connections form almost exclusively in the ipsilateral motor domain (dorsal neuropil) of the VNC. The distribution of these postsynaptic connections vary along the anteroposterior and mediolateral axis, which likely correspond with the myotopic organisation of motor neuron dendrites in the dorsal neuropil [@Landgraf2003].



![**Neurons of the A02 lineage have similar morphology.** Morphology of (**A**) A02e, (**B**) A02f and (**C**) A02g within the first abdominal segment, reconstructed in a TEM volume of the L1 nervous system. Synaptic input, orange; synaptic output, blue. Top panel, transverse view; bottom panel, dorsal view.](./figures/thesis_aim2_3a.svg){#fig:A2_3a}

A02e makes the majority of its synapses (summarised in [@fig:A2_3b]A) with motor neurons innervating the VL muscles, specifically MN13 (16 per hemisegment, 24.8% of total output), MN30 (12 per hemisegment, 18.6% of total output) and MN12 (8 per hemisegment, 12.4% of total output).  Similarly, A02g predominantly synapses onto motor neurons innervating VL muscles MN13 (16 per hemisegment, 26.2% of total output), MN30 (17 per hemisegment, 27.9% of total output) and MN12 (4.5 per hemisegment, 7.4% of total output).

However, A02e and A02g differ in that A02e also makes a significant proportion of its outputs to motor neurons innervating DL muscles, like MN4 (5.5 per hemisegment, 8.5% of total output), MN10 (4.5 per hemisegment, 7% of total output), MN3 (4 per hemisegment, 6.2% of total output) By contrast, A02g forms the remainder of its synapses with motor neurons innervating the VO muscles, like MN15/16 (5 per hemisegment, 8.2% of total output) and MN15/16/17 (6 per hemisegment, 9.8% of total output; [@fig:A2_3b]A).

A02f shares most similarities with A02e, innervating MN4 (7.5 per hemisegment, 20.3% of total output) and MN10 (3.5 per hemisegment, 9.5% of total output), both of which project to the DL muscles. However, A02f also has unique outputs to the LT projecting motor neurons, MN22/23 (6 per hemisegment, 16.2% of total output) and MN21/22 (2 per hemisegment, 5.4% of total output), as well as the DO projecting motor neuron, MN19 (3.5 per hemisegment, 9.5% of total output; [@fig:A2_3b]A).

Interestingly, A02e and A02g innervate similar patterns of motor neurons as the previously reported Saaghi-1 neuron [@Heckscher2015] ([@fig:A2_3b]A). Disrupting the endogenous activity of Saaghi neurons was shown to induce left-right asymmetric posture during persistaltic crawling. As such, these published results will make for an interesting comparison to our own behavioural assays.

All 3 neurons also make premotor-to-premotor connections, but those are not reported here.



![**A02 neurons innervate different groups of motor neurons.** (**A**) Number of synapses formed from premotor neuron (left) to motor neuron (top), as observed within a single abdominal segment of a TEM volume. Identidy of the muscles anatomically downstream of (**C**) A02e, (**D**) A02f and (**E**) A02g compared to (**B**) reference musculature. Colour indicates the number of (red) contralaterel and (blue) ipsilateral synapses made with the corresponding MN.](./figures/thesis_aim2_3b.svg){#fig:A2_3b}



### A02e and A02f are sufficient to delay onset of nocifensive behaviour

To test the relative involvement of the different A02 populations in escape behaviour, we performed optogenetic co-activation of Basin neurons with each of the A02 lines. Given the relative similarity in connectivity between A02e and A02g, we expected these neurons to present the greatest similarity in phenotype.

Consistent with our previous observations, lines expressing A02e showed a delayed peak in roll percentage ([@fig:A2_4]A). We quantified this delay as the 'latency to roll'. We saw significant increases in latency to roll for lines with expression in A02e (*1816*, *p* < .001, *r* = .326, *1817*, *p* < .001, *r* = .290) and A02f, *p* < .001, *r* = .202, compared to a driver control (*attp2;Basin>CsChrimson*; [@fig:A2_4]D). 

Further, to determine whether this delay in roll onset reflected a delay in our descriptive metrics, we quantified the latency to crabspeed and latency to curve (defined as the time between stimulus onset and rise in respective metric). Latency to crabspeed was significantly increased for A02f, *p* < .001, *r* =  .291, and for both A02e lines, *1816*, *p* < .001, *r* = .523 and *1817*, *p* < .001, *r* = .475 ([@fig:A2_4]F). All 3 neurons showed an increase in latency to curve, but this effect was greatest for A02e (*1816*, *p* < .001, *r* = .648 and *1817*, *p* < .001, *r* = .660) and A02f (*1792*, *p* < .001, *r* = .344; [@fig:A2_4]H). Together, these results demonstrate that ectopic activation of either A02e or A02f induces a significant delay to both the onset of rolling and C-shape bending, the latter indicated by larval curvature. 

Consistent with our previous data, A02e also showed a significant reduction in average curvature across the stimulation bout, *1816*, *p* < .001, *r* = .648 and *1817*, *p* < .001, *r* = .493 ([@fig:A2_4]I). Interestingly, both A02f and A02g also showed significant reductions in average curvature, but with a smaller magnitude of change. Similarly, all lines tested showed significantly reduced average crabspeed ([@fig:A2_4]G). Only lines labelling A02e showed a significant decrease in total roll duration, *1816*, *p* < .001, *r* = .277 and *1817*, *p* = .029, *r* = .148, however the size of this effect was relatively small ([@fig:A2_4]E).

These results suggest that all the A02 neurons tested are implicated in the performance of escape behaviours, but that A02e and A02f modulate the most similar aspects of behaviour. Specifically, activation of A02e and A02f delays the onset of both C-bend and roll behaviours. While the overall presentation of rolling seems largely unaffected (equivalent roll durations), reduced average curvature suggests the presentation of C-bending is reduced in all lines.




![**A02 neurons differentially modulate escape behaviour.** Optogenetic co-activation of Basin neurons with different A02 neurons with irradiance 100&mu;W/cm^2^. Instantaneous roll proportion for (**A**) A02e, (**B**) A02f and (**C**) A02g. (**D**) Average latency to the first bout of rolling. Average latency to initial rise in (**F**) crabspeed and (**H**) curve. (**E**) The average total duration of rolls per larvae, (**G**) average crabspeed and (**I**) average curvature of larvae during stimulation. Horizontal orange bar, stimulation bout. Error bars, 95% confidence interval. *n*, indicated in plot. \* *p* < 0.05, \** *p* < 0.01, \*** *p* < 0.001.](./figures/thesis_aim2_4.svg){#fig:A2_4}



### A02 neurons show minimal modulation of basal locomotion

Our previous data had illustrated that A02e showed behaviour-specific modulation of larval posture, so we wanted to determine whether the other A02 neurons showed similar behavioural specificity. To do this we performed either optogenetic activation or silencing (TNT) of the A02 neurons during normal exploratory behaviour. 

For all lines, there was an overall trend toward a decrease in crawl frequency when activated  ([@fig:A2_5]B), which was mirrored by a general increase in crawl frequency when silenced ([@fig:A2_5]E). This is consistent with previous literature, which implicate the A02 population in regulating peristaltic frequency [@Kohsaka2014]. However, while significant, the size of effect from these manipulations was negligible. Genotypes showing a decrease in crawl frequency also showed a decrease in crawl amplitude but, again, the magnitude of this effect was benign ([@fig:A2_5]A). 

Notably, activation of A02f caused a large and significant increase in curvature during stimulation, *p* < .001, *r* = .495 ([@fig:A2_5]C). Specifically, activation of A02f induces a decrease in the percentage of animals crawling ([@fig:supp4]B), followed by an increase in curvature 5 seconds after the onset of stimulation ([@fig:supp4]A). Similarly, activation of *4189* (A02g) also induces a significant increase in curvature, *p* < .001, *r* = .211, but with relatively small magnitude ([@fig:A2_5]C). Silencing A02 neurons gave significant decreases in average curvature for *1792* (A02f), *p* = .016, *r* = .138, *1817* (A02e), *p* < .001, *r* = .217, and *4189* (A02g), *p* < .001, *r* = .186, but the size of these effects was also negligible. 

These results suggest that none of the neurons in questions are necessary for the performance of crawling behaviour. The only interesting observation was that ectopic activation of A02f induced curved posture. By extension, this may implicate the endogenous activity of lateral transverse muscles, which are downstream of A02f, as necessary for maintaining left-right symmetry. However, whether this asymmetry reflects discrete unilateral behaviours (e.g. head casting), or just asymmetric gait, is unclear from these analyses. 

![**Endogenous A02 activity is not necessary for basal locomotion.** (**A-C**) Optogenetic activation of A02 neurons with irradiance 600&mu;W/cm^2^. (**A**) The average crawl amplitude, (**B**) crawl frequnecy and (**C**) curvature of larvae during optogenetic stimulation. (**D-F**) Silencing of A02 neurons with TNT. (**D**) The average crawl amplitude, (**E**) crawl frequnecy and (**F**) curvature of larvae during free exploration. Error bars, 95% confidence interval. *n*, indicated in plot. \* *p* < 0.05, \** *p* < 0.01, \*** *p* < 0.001.](./figures/thesis_aim2_5.svg){#fig:A2_5}




## Aim 3.1

Throughout the literature there are numerous methods which implement different algorithms for the detection of discrete behaviours, like rolling. The extent to which these pipelines reach consensus in the scoring of like-named behaviours is unknown. We wanted to assess whether the phenotypic differences observed for rolling behaviour with A02e, originally scored using the Salam pipeline, would be consistently identifiable across 2 other established behavioural pipelines; JB and JAABA.

### A02e phenotype is detectable regardless of analytical method

While the JB pipeline already has a pre-trained classifier for detection of rolling behaviour, we had to train a novel roll classifier for JAABA (Shua Noh, unpublished). We processed our optogenetic co-activation experiments for A02e, as well as the driver control (*1816,Basin>CsChrimson* and *attp2;Basin>CsChrimson*, respectively), with each of the different classification methods. 

The three pipelines showed visible differences in the scoring of roll behaviours for our control data, which serves as our baseline for quantification of escape behaviour. Salam showed the most sparse scoring of rolling behaviour per larvae ([@fig:A1_4]A), whereas JAABA showed the most abundant scoring ([@fig:A1_4]C). This is reflected by the variation in average time-spent rolling, Salam, *M* = 2.50 seconds, JB, *M* = 4.03 seconds and JAABA, *M* = 7.56 seconds, per larva ([@fig:A1_4]H).

When comparing A02e co-activation to the control, Salam demonstrated the expected delay in roll onset, but otherwise shows a remarkably similar percentage of rolling throughout stimulation ([@fig:A1_4]D). By contrast, both the JB and JAABA show a considerable decrease in the percentage of animals rolling during the stimulation bout ([@fig:A1_4]E,F). This was corroborated by the dramatic decreases in time spent rolling, specifically for JB and JAABA ([@fig:A1_4]H).

Importantly, we observed an increase in the latency to roll for Salam, *p* < 0.001, *r* = .326, JB, *p* < 0.001, *r* = .662 and JAABA, *p* < 0.001, *r* = .733, with our A02e co-activation data ([@fig:A1_4]G). This suggests that the phenotype we had originally observed with Salam is consistent and robust, rather than an artefact from our choice in method.



![**A02e phenotype is consistent across classification methods, despite differences in baseline scoring.** (**A-C**) Optogenetic activation of Basin neurons (*Basin>CsChrimson*) with irradiance 100&mu;W/cm^2^. Ethogram indicating bouts of rolling behaviour as scored by the (**A**) Salam, (**B**) JB and (**C**) JAABA pipelines, apposed to bouts of crawling scored by Salam. (**D-F**) Optogenetic co-activation of Basin neurons with A02e (*1816*) or a driver control (*attp2;Basin>CsChrimson*). Instantaneous roll proportion scored by the (**D**) Salam, (**E**) JB and (**F**) JAABA pipelines. (**G**) Latency to roll and (**H**) average time-spent rolling by pipeline. Horizontal orange bar, stimulation bout. Error bars, 95% confidence interval. *n*, indicated in plot. \* *p* < 0.05, \** *p* < 0.01, \*** *p* < 0.001.](./figures/thesis_aim1_4.svg){#fig:A1_4}



### Pipelines vary in accuracy and specificity of scoring

Given the magnitude of difference in scored rolling between pipelines, we wanted to understand their relative accuracy and specificity. To assess this, we manually scored 1 timestamp consisting of 33 larvae, for two different aspects of escape behaviour. We scored both C-bending behaviour (initiation & maintenance of C-shape posture) against rolling behaviour (C-shape posture coincident with lateral movement) as mutually exclusive behaviours (see Methodology). Distinguishing these two behaviours allowed us to evaluate the specificity of either pipeline for rolling versus escape behaviours more generally.

We quantified the performance of the pipelines by their percentage overlap with the ground truth, as well as the duration of false positives scored (summarised in [@fig:A1_5]A). Salam demonstrated the lowest specificity for rolling, labelling 24% of true rolls and 26% of true C-bends ([@fig:A1_5]B). The JB pipeline showed the greatest specificity for scoring rolling, labelling 56% of true rolls compared to just 15% of true C-bends. JAABA also showed improved specificity versus Salam, labelling 87% of true rolls and only 41% of true C-bends ([@fig:A1_5]B).

When assessing false positives, it is important to note that falsely detected 'rolls' frequently overlap with true C-bend behaviours. As such, we can assess false positives against rolls separately from false positives against general nocifensive behaviours (combination of roll & C-bend). The JB pipeline demonstrates the greatest accuracy, scoring the fewest false positives for either rolling (.59 seconds per larvae) or nocifensive behaviour generally  (.17 seconds per larvae). Salam and JAABA performed with similar accuracy, scoring false positive rolls at 1.39 and 1.86 seconds per larvae, respectively ([@fig:A1_5]C). Both showed greater accuracy when scoring against nocifensive behaviour in general, scoring fewer than .85 seconds per larvae of false positive behaviour ([@fig:A1_5]C).

These results argue that JB offers best trade off for specificity and accuracy against proportion of behaviours detected. Otherwise JAABA offers the greatest absolute scoring of rolling, but at the cost of some specificity and accuracy.

![**Roll classifiers vary in specificity and accuracy.** Optogenetic activation of Basin neurons, only, with irradiance 100&mu;W/cm^2^. (**A**) Average duration of rolls scored per larva, by method of scoring. Bars are split by the duration of overlap with ground truth for C-bend and roll. (**B**) The proportion of overlap for classified rolling behaviours, by pipeline, against ground truth scoring for C-bending, rolling or both (roll & C-bend combined). (**C**) The average duration of false positive rolls scored per larvae for each of the pipelines, as compared against ground truth scoring for rolling or escape behaviour generally (roll & C-bend combined).](./figures/thesis_aim1_5.svg){#fig:A1_5}



# Discussion

The overall objective of this study was to identify and characterise novel interneurons involved in the performance of nocifensive behaviours. Optogenetic behavioural screening allowed us to describe 3 groups of neurons that affected changes to the presentation of escape behaviours. Among these are the inhibitory premotor A02e neurons, previously identified as anatomically downstream of key escape-sufficient interneurons. We provide detailed characterisation of A02e neurons in the performance of both nocifensive and basal locomotor behaviours. A02e demonstrated activity-dependent modulation of posture during nocifensive, but not basal behaviours, implying some degree of behaviour-specific recruitment. 

Our secondary objective was to try and characterise the relationship between anatomic connectivity and locomotor involvement across different premotor interneuron populations. We identified two PMNs that were lineage-related to A02e, which displayed overlapping but unique patterns of anatomic connectivity. Behavioural assays demonstrated that ectopic activation of PMNs upstream of dorsal and lateral muscle groups, but not ventral muscle groups, induced a delay to the initiation of escape behaviours. This suggests that dorsal and lateral muscles are potentially critical for early-presenting nocifensive behaviours, namely C-shape bending. 



## A02e is downstream of known nociceptive circuitry

We have demonstrated that ectopic manipulation of A02e activity modulates larval posture during escape behaviours. However, we do not know if A02e is normally recruited during escape. Some evidence, from neuronal reconstruction, supports the idea that A02e may be recruited by nocifensive circuitry. A02e is monosynaptically innervated by the second-order nociceptive sensory neurons Down-and-Back (DnB, or A09l), which are sufficient to trigger nocifensive behaviours [@Burgos2018] ([@fig:circuitry]). Silencing DnB neurons with a TNT construct leads to a decrease in the percentage of time that larvae spend rolling as well as reduced curvature of larvae during escape behaviours. 

DnB neurons are cholinergic and thus excitatory neurons, suggesting that they activate A02e neurons to elicit escape behaviours. As such it is surprising that *activation* of A02e neurons, as performed in this study, or *silencing* of DnB neurons (preventing DnB-directed activation of A02e neurons) would result in the same phenotype - reduced body curvature.

A possible explanation for this concerns the inherent left-right asymmetry synonymous with escape behaviour. Given that the first movement produced during escape is a unilateral bending of the head and tail, muscle contraction should be asymmetric [@Lahiri2011]. Therefore MN activation and presumably also PMN activation should present asymmetry. It is possible that endogenous activity of DnB neurons evokes asymmetric activity of A02e neurons, that may promote the performance of escape behaviours. By contrast, our optogenetic manipulations bilaterally activate A02e neurons. As A02e neurons directly inhibit motor neurons (for DL and VL muscles), such bilateral inhibition may well be incompatible with the performance of C-bending behaviour.

Further, our data supports the notion that A02e neurons are, in fact, recruited during escape behaviours. We observed that silencing A02e neurons lead to an increase in both nocifencive curvature and time-spent rolling. This suggests that, while A02e neurons are not strictly necessary for  the performance of escape behaviours, endogenous A02e activity does actively modulate nocifensive posture. Thus, the anatomic and behavioural data implicate A02e as part of the premotor circuitry recruited and required for the stereotypic presentation of larval nocifensive behaviours.



## Behavioural specificity of A02e neurons

Recently it has been shown that, *all* of the larval somatic muscles in a given abdominal segment are active during peristaltic crawling [@Zarin2019a]. Therefore, the performance of alternative behaviours cannot be conferred by behaviour-specific musculature. Rather, this is presumably determined by recruiting motor cohorts in specific spatial and temporal patterns. This likely involves the activation of behaviour-specific premotor neurons [@Zarin2019a;@Kohsaka2019]. To test whether A02e showed such behaviour-specificity, we performed ectopic manipulation of A02e neurons during basal locomotor behaviours.

Increases in the postural metric 'curvature' is indicative of unilateral bending during escape behaviours. During basal locomotion, measures of curvature instead reflect the frequency and magnitude of baseline turning and head casting behaviours. Our data showed that ectopic activation of A02e decreases curvature during escape behaviours, but did not affect curvature for basal locomotion. This suggests that, for unilateral bending behaviours, A02e may be specifically recruited during escape behaviours.

Interestingly, there is evidence indicating that baseline turning behaviours may not require nervous control at all. Recent investigation produced a biomechanical model of *Drosophila* larvae, which limited the neural circuitry to simple proprioceptor-to-motor neuron motifs [@Loveless2019]. Despite a lack of circuitry for the sensation or activation of bending motions, model larvae were able to produce normal turning behaviours. This suggested a purely mechanical model of the larva’s body was sufficient to facilitate unilateral bending during basal locomotion [@Loveless2019]. Therefore it's possible that neural circuitry for the performance of unilateral nocifensive bending, including A02e, is not necessary for basal locomotor bending.

Previous studies have implicated A02e neurons in the coordination of peristaltic crawling [@Kohsaka2014;@Kohsaka2019]. Ifb-Fwd neurons, which are active during forward crawling, promote activation of transverse muscles and inhibit contraction of longitudinal muscles, thus preventing the simultaneous activation of antagonistic motor cohorts [@Kohsaka2019]. This longitudinal muscle inhibition is mediated by 4 pairs of neurons, one of which are the A02e neurons. Our manipulations of A02e during basal locomotion show minimal changes to peristaltic amplitude and frequency, suggesting that A02e neurons may well show redundancy in this circuit. As such, our data supports the hypothesis that A02e neurons affect greater influence in the modulation of escape behaviours, as opposed to crawling behaviours.



## Implication of motor cohorts for escape behaviours

While detailed motor profiles have been constructed for larval crawling behaviours [@Heckscher2012;@Zarin2019a], few muscles have been implicated in the performance of either C-bending or rolling behaviours. We performed behavioural assays for PMNs upstream of different motor cohorts, allowing us to predict which muscle groups may be more or less important for these behaviours.

We sought to compare the behavioural phenotype of premotor neurons upstream of overlapping, yet distinct motor cohorts. To do this we assayed the affects of optogenetic activation on three lineage-related inhibitory PMNs, A02e, A02f and A02g, on the performance of escape behaviours. The most striking observation was that activation of either A02e or A02f, but not A02g, increased the latency to the onset of rolling behaviour. In spite of this, larvae for all lines did eventually produce the full repertoire of escape behaviours, suggesting that the endogenous activity of these neurons is not strictly necessary for their performance.

A02e and A02f share downstream targets in the dorsal longitudinal (DL) muscles, which are not downstream of A02g. This suggests that the DL muscles may be recruited during the initiation of escape behaviours, perhaps more specifically for the performance of C-bending behaviours. Consistent with this theory, the lateral-most of these DL muscles (muscles 3 & 4) are also downstream of the Saaghi-1 neuron, which has previously been implicated in the maintenance of left-right symmetry during basal locomotion [@Heckscher2012]. 

However, we cannot rule out the possibility that the delayed onset of C-bending actually stems from the inhibition of different cohorts of muscles. A02f is unique for being the only neuron assayed that is upstream of lateral transverse (LT) muscles. LT muscles have previously been identified as critical for self-righting behaviours, which share similar motions to nocifensive rolling [@Picao-Osorio2015]. Thus it is plausible that activation of A02f, and thus inhibition of LTs, disrupts the onset of C-bending. Consistent with this, our single activation of A02f neurons increased the presentation of curvature during basal locomotion.

Implication of LT muscles in C-bending is corroborated by the fact that LT-projecting motor neurons receive direct innervation from two populations of escape-sufficient, second order sensory neurons, mCSI [@Yoshino2017] and DnB neurons [@Burgos2018]. At present, these represent the shortest paths between sensory and motor neurons within the nocifensive circuitry  (2 and 3 synapses, respectively), suggesting LT muscles may well be the first muscles activated during escape.

A02g was the only neuron assayed to be upstream of the ventral orbital (VO) muscles. Given that activation of A02g induced no change in behaviour latency, we would predict that the VO muscles likely play little role in the initiation of escape behaviours. 



## Analytical methods for quantifying escape behaviours

Within *Drosophila* research, there are numerous methods for the quantification of larval escape behaviours. The most sophisticated of these rely an algorithmic detection of behaviours. Some of these pipelines are built using user-written behavioural definitions [@Ohyama2013], while others implement supervised machine learning methods to train behaviour classifiers [@Kabra2013;@Jovanic2017]. Regardless of design, each algorithm is either programmed or trained based on subjective, user-defined annotations of larval behaviours. The degree to which these different pipelines achieve consensus in the labelling of like-named behaviours is unknown. We sought to evaluate whether there were discrepancies in the scoring of rolling behaviour across different pipelines. In particular we wanted to determine whether the modulation of escape behaviours affected by A02e was detectable outside our particular methodology.

Encouragingly, the increase in latency to roll upon A02e co-activation was detectable and significant across all pipelines. This allowed us to rule out the possibility that the observed phenotype is an artefact of our methodology. Notably, the magnitude of this increase was considerably different across the 3 pipelines. These differences may reflect the different feature sets employed by either pipeline to score behaviour. For instance, we know that ectopic A02e activation decreases larval curvature. Given that Salam scores rolling exclusively using the crabspeed metric [@Ohyama2013], this curvature change may not affect Salam's scoring of rolling. However, JB and JAABA generate numerous per-frame and window metrics to score behaviour [@Kabra2013;@Masson2020], therefore changes in scoring of rolling may also reflect changes in curvature.

While we generalise this argument in terms of the curvature metric, it is entirely possible that the features causing this difference in rolling behaviour reflect metrics or motor changes we have not yet identified. As such, to better understand how PMN activity might subtly modulate the performance of escape behaviours, it may be interesting to identify and isolate the salient features calculated by these pipelines.

Our data also demonstrate that Salam, JB and JAABA showed a different baseline scoring of roll behaviour, as indicated by the differences in time-spent rolling for control animals. To evaluate the relative performance between these pipelines, we compared their relative accuracy and specificity to a ground truth. This indicated that JB scored behaviours with the greatest specificity for rolling, while JAABA showed the greatest overlap with the ground truth. 

From these comparisons, we should be able to increase the overall accuracy of future behaviour quantification by switching to either the JB or JAABA pipeline. The choice between these pipelines, then, will depend on the hypotheses to be tested.



## Limitations

One analytical constraint in this study was our ability to resolve specific motions, or components, of escape repertoire. While we largely characterise C-bending and rolling in this thesis, these behaviours are typically interspersed with a range of other complex motor behaviours, including changes of direction, head lifting, tail lifting and 'bend-crawls'. At present, we only have automated detection methods for one of these behaviours.

In lieu of discrete behavioural classification, we inferred C-shape bending using the postural metric 'curve', as calculated by the Choreography package [@Swierczek2011]. However larvae can display high curvature separately with a head bend, tail bend or from a coincident head and tail bend either in the same direction (C-shape) or opposite directions (S-shape). While our observations of decreased curvature still likely represent decreases in C-shape posture, modulation of alternative motions may have compounded this result.

Similarly, while our definition of rolling behaviour is delineated by crabspeed, the strictest definition of a roll requires that an identifiable body landmark (commonly the trachea) rotate through 360&deg;C around the anteroposterior axis. Unfortunately, the system we implement for our behaviour assays (MultiWorm Tracker, MWT [@Swierczek2011]) outputs larval outlines, rather than video, preventing this quantification.

While an increased feature set would have allowed for a more comprehensive analysis of our premotor neuron screen, our present selection of features was sufficient to identify split-GAL4 lines affecting robust modulation of nocifensive behaviours. Further, the methods used here are in line with those reported across the field [@Jovanic2016;@Yoshino2017;@Burgos2018;@Masson2020]. However in future experiments, to reduce the ambiguity of detected phenotypes, it may be beneficial to focus more on descriptive metrics (e.g. head or tail angle/velocity, etc), rather than discrete classification of subjective behaviours.

Another factor limiting the interpretation of our results pertains to the inferences of functional connectivity, based on anatomical connectivity. For example, while A02e makes 16 inhibitory synapses per hemisegment onto MN13, this does not guarantee that MN13 shows reduced activity when A02e is optogenetically stimulated. This is due to the fact that we cannot infer the efficacy of the connection from synapse number alone, nor can we tell which other inputs to the motor neuron may be active during stimulation of escape behaviours. Specifically, our prediction that VO muscles are not important for the initiation of escape behaviour may be a false negative, where A02g-directed inhibition of VO motor neurons may not be sufficiently efficacious to affect behavioural change. 



## Future directions

A few key sets of experiments would greatly complement the research in this study. This first is the development of a motor profile for escape behaviours. This has already been achieved for crawling behaviours by imaging muscle calcium transients, a proxy for muscle activation, across all abdominal segments in the larva [@Zarin2019a]. Conducting this imaging for escape behaviours is complicated by the movement of muscles in the z-axis, particularly during rolling behaviours. However the use of split-GAL4 lines labelling discrete muscle populations, or the use of fillet preparations may help facilitate this work. This would prove an invaluable tool, as determining functionally co-active groups of muscles will allow for predictions of critical pattern-generating circuits, based on anatomical connectivity.

Further, it will become important to establish the functional connectivity of the PMNs identified. For instance, it would be interesting to evaluate whether these neurons are indeed activated by presentation of naturalistic nociceptive stimuli, or by optogenetic activation of upstream partners. Similarly, questions remain regarding the endogenous spatial and temporal patterns of activation of both PMNs and MNs. Do PMNs show different patterns of recruitment along the anteroposterior or left-right axes? In what order are PMNs recruited during nocifensive behaviours? These questions will be best addressed with functional studies imaging the activity of PMNs and MNs during the activation of escape behaviours. Ideally this would be tested by *in vivo* imaging of neural activity, perhaps by restraining larva in microfluidic devices [@Ghaemi2015;@Ghaemi2017]. However if a fictive nocifensive locomotor paradigm can be developed, similar to those for crawling behaviours [@Lemon2015;@Pulver2015], the same questions could be addressed in a dissected preparation.



# Conclusion

Here, we identify the inhibitory A02e neurons as part of the premotor circuitry involved in the performance of escape behaviours, in *Drosophila* larvae. We show that larval posture, namely curvature, is modulated in an activity-dependent manner by A02e neurons. While A02e has also been shown to be part of circuitry linked to crawling behaviour, we did not observe any changes to basal locomotion when perturbing the function of A02e. This suggests that larval premotor circuits for distinct behaviours show anatomic overlap, but that certain component neurons may show behaviour-specific redundancies. 

Further, we show that inhibitory premotor neurons upstream of lateral and dorsal muscles, but not those upstream of ventral muscles, actively disrupt the onset of larval escape behaviour. This suggests that the DL and LT muscles are necessary for the performance of early-presenting escape behaviours, namely C-shape bending. Together, these findings offer novel insights into the circuit mechanisms distinguishing larval nocifensive behaviours from other basal behaviours.



# Bibliography

\singlespacing

<div id="refs"></div>

\doublespacing

# Supplemental material



\newcounter{suppfigure}

\setcounter{suppfigure}{1}

\renewcommand*{\thefigure}{S\arabic{suppfigure}}


![**Relates to [@fig:A2_1].** (**A**) Instantaneous crawl percentage and (**B**) roll percentage, upon Basin activation, at two different light irradiances (100&mu;W/cm^2^ and 600&mu;W/cm^2^). Horizontal orange bar, stimulation bout.](./figures/thesis_supp3.svg){#fig:supp2}

\stepcounter{suppfigure}

![**Relates to [@fig:A2_2].** (**A**) Curvature and (**B**) instantaneous crawl percentage of *4232>CsChrimson* compared to a driver control, *attp2>CsChrimson*. Stimulation irradiance, 600&mu;W/cm^2^. Horizontal orange bar, stimulation bout.](./figures/thesis_supp4.svg){#fig:supp3}

\stepcounter{suppfigure}

![**Relates to [@fig:A2_5].** (**A**) Curvature and (**B**) instantaneous crawl percentage of *A02f>CsChrimson* compared to a driver control, *attp2>CsChrimson*. Stimulation irradiance, 600&mu;W/cm^2^. Horizontal orange bar, stimulation bout.](./figures/thesis_supp5.svg){#fig:supp4}

