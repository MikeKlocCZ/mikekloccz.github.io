---
title: "Dynamical Modelling with Neural Differential Equantions"
excerpt: "Optimization problems in biology and physics <br/><img src='/images/method_control.png'>"
collection: projects
---

## A Model is Worth a Thousand Data Sets


There are two fundamental ways how we can try to understand  dynamical phenomena in Nature. The traditional one is based on mathematical modelling. We look at the system of interest, strip away "all unnecessary features" whose contribution to the dynamics are "of lower orders" and build a mechanistic model under these simplifying conditions. Such models can be very powerful for qualitative understanding of mutual interactions between the actors in the system, but due to the simplifications, quantitative predictions might  deviate from reality. An example from physics could be the [Ising model](https://en.wikipedia.org/wiki/Ising_model) of magnetization. In its simplest 2D form, the microscopic magnetic moments (spins) are placed on a two-dimensional lattice and only short-range (nearest-neighbor) interactions are considered. Thus, the minimal-energy state is associated with all spins aligned, i.e., a ferromagnetic state. By introducing temperature $$T$$ , the system starts to be exposed to thermal fluctuations which increase  with $$T$$, and at some point they might completely break the ferromagnetic order. If one follows the mean magnetization  over the ensemble of individual spins with (Boltzmann distribution)[https://en.wikipedia.org/wiki/Boltzmann_distribution], one finds that there is a second-order phase transition at certain critical  [(Curie) temperature](https://en.wikipedia.org/wiki/Curie_temperature) $$T_c$$ where magnetization completely disappears. This phenomenon is indeed observed in natural ferromagnets and the Ising model gives a good understanding of the competition between the spin-spin interaction enforcing magnetic order and the thermal noise acting against it. From the model, one can also deduce the critical temperature $$T_c$$. Its value, however, is difficult to link directly to real materials since too many simplifications were used. 

Systems biology represents a similar mechanistic approach. The regulation of a target gene $$Y$$ via a transcription factor $$X$$ is often linked through the [Hill function](https://en.wikipedia.org/wiki/Hill_equation_(biochemistry)). This relation is derived from mass action kinetics and does not take into account any detailed biophysical features of the DNA binding. As a result, there is a simple relation from $$X \to Y$$ which only takes a few parameters (concentration of $$X$$, promoter strength and degree of cooperativity). With this obviously simplified approach one can already build [principles of gene regulatory networks](https://books.google.ch/books?id=tcxCkIxzCO4C&printsec=frontcover&redir_esc=y#v=onepage&q&f=false) and understand the designs of network motifs and their function. On the other hand, direct quantitative predictions for complex biological systems are still limited.


A different way is to learn our insights purely from statistical analysis of the data.


## Optimal Control Problems


<figure>
  <img src="/images/ControlQubit.png" alt="Optimal control scheme for qubit state preparation">
  <figcaption>Figure 1: Example of optimal control learnt using neural stochastic differential equations.</figcaption>
</figure>