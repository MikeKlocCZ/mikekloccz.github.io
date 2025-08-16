---
title: "Dynamical Modelling with Neural Differential Equations"
excerpt: "Optimization problems in biology and physics <br/><img src='/images/method_control.png'>"
collection: projects
---

## A Model is Worth a Thousand Data Sets


There are two fundamental ways how we can try to understand  dynamical phenomena in Nature. The traditional one is based on *mathematical modelling*. We look at the system of interest, strip away "all unnecessary features" whose contribution to the dynamics are "of lower orders" and build a mechanistic model under these simplifying conditions. Such models can be very powerful for qualitative understanding of mutual interactions between the actors in the system, but due to the simplifications, quantitative predictions might  deviate from reality. An example from physics could be the [Ising model](https://en.wikipedia.org/wiki/Ising_model) of magnetization. In its simplest 2D form, the microscopic magnetic moments (spins) are placed on a two-dimensional lattice and only short-range (nearest-neighbor) interactions are considered. Thus, the minimal-energy state is associated with all spins aligned, i.e., a ferromagnetic state. By introducing temperature $$T$$ , the system starts to be exposed to thermal fluctuations which increase  with $$T$$, and at some point they might completely break the ferromagnetic order. If one follows the mean magnetization  over the ensemble of individual spins with (Boltzmann distribution)[https://en.wikipedia.org/wiki/Boltzmann_distribution], one finds that there is a second-order phase transition at certain critical  [(Curie) temperature](https://en.wikipedia.org/wiki/Curie_temperature) $$T_c$$ where magnetization completely disappears. This phenomenon is indeed observed in natural ferromagnets and the Ising model gives a good understanding of the competition between the spin-spin interaction enforcing magnetic order and the thermal noise acting against it. From the model, one can also deduce the critical temperature $$T_c$$. Its value, however, is difficult to link directly to real materials since too many simplifications were used. 

Systems biology represents a similar mechanistic approach. The regulation of a target gene $$Y$$ via a transcription factor $$X$$ is often linked through the [Hill function](https://en.wikipedia.org/wiki/Hill_equation_(biochemistry)). This relation is derived from mass action kinetics and does not take into account any detailed biophysical features of the DNA binding. As a result, there is a simple relation from $$X \to Y$$ which only takes a few parameters (concentration of $$X$$, promoter strength and degree of cooperativity). With this obviously simplified approach one can already build [principles of gene regulatory networks](https://books.google.ch/books?id=tcxCkIxzCO4C&printsec=frontcover&redir_esc=y#v=onepage&q&f=false) and understand the designs of network motifs and their function. On the other hand, direct quantitative predictions for complex biological systems are still limited.


A different way is to learn our insights purely from *statistical analysis of the data* that we collect from the system. Over the past two decades, this approach has become increasingly important across many research fields, thanks to major improvements in how we collect large data sets. In molecular biology, this has been  represented, for example, by the development of sequencing technologies that generate genome-wide data, now also with single-cell or spatial resolutions. A lot of development has beed done on optimisation of statistical methods and tools for analysis of such data. The growing demand for more quantitatively trained researchers has drawn many of us—from traditional systems biology, computer science, or physics—into the fields of bioinformatics and computational biology (myself included). Statistical inference can answer important questions like "which genes are differentially expressed upon treatment", or "what are the putative ligand-receptor interactions that drive the observed transcriptional changes", but it does not provide direct mechanistic insight.

There can, however, be a *third way* trying to meet half-way between the world of mathematical modelling and data science. The idea is to use the existing  models that contain already lots of understanding of the dynamics of the system, and use data to either improve the model's predictive capacity or to adapt it for a certain task (e.g., control problems). This approach is known as [Scientific Machine Learning (SciML)](https://sciml.ai) and a path to it was paved mainly by this [paper](https://arxiv.org/abs/1806.07366) introducing Neural Ordinary Differential Equations (neural ODEs). The core observation in the paper was that so-called residual networks (ResNets), which were originally introduced to deal with vanishing gradient problems, actually have the same structure as the Newton's method of a numerical solution of an ODE. Thus, if one stacks "infinite" number of these layers in the network architecture, all these layers can be replaced by the ODE itself. This step brought dynamical modelling and machine learning onto a same platform, making it possible to combine differential equations with neural networks seamlessly.

Next, I will introduce two projects that use SciML for optimal control and model discovery.

## Optimal Control Problems


<figure>
  <img src="/images/ControlQubit.png" alt="Optimal control scheme for qubit state preparation">
  <figcaption>Figure 1: Example of optimal control learnt using neural stochastic differential equations.</figcaption>
</figure>


## Decoding ER$$\alpha$$-GATA3 regulation in ER positive breast cancer


<figure>
  <img src="/images/er_gata.png" alt="Optimal control scheme for qubit state preparation">
  <figcaption>Figure 2: Example of optimal control learnt using neural stochastic differential equations.</figcaption>
</figure>


