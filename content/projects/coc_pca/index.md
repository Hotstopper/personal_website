---
title: "Principal Component Analysis on Clash of Clans Troops"
date: 2024-08-19
draft: false
---
{{< social "github" "https://github.com/Hotstopper/coc_troop_stats_pca" >}}

A fun exercise in Principal Component Analysis (PCA) for dimensionality reduction. 

I collected data of different troop attributes in the mobile game, Clash of Clans. These included damage per attack, range, hitpoints etc.

PCA uncovers the main latent traits that differentiates units. 

For example, the First Principal Component has a coefficient of 0.48 on hitpoints but -0.16 on range and -0.39 on movement speed. So I interpret this as a measure of "tankiness", and describes troops like golem and PEKKA.

The Second Principal Component has a coefficient of 0.65 on range but -0.026 on hitpoints. So I interpret this as a measure of "range" and representative of troops such as archers and e-drags.

The results are plotted below.
{{< figure src="coc.png" alt="PCA of Clash of Clans Troop Attributes" caption="PCA of Clash of Clans Troop Attributes" >}}

---