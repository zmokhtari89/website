+++
title = "K-Means Klang: Audio Clustering"
description = "Unsupervised discovery of acoustic patterns in music."
date = 2026-05-04
weight = 2

[extra]
thumbnail = "/projects/project-three/thumb.png"
tags = ["Unsupervised Learning", "Tensorflow", "Docker", "Streamlit", "GCP", "FastAPI"]
+++

## Problem

Music is conventionally organised by genre, but acoustically similar tracks often cross genre lines. We asked: can unsupervised learning find structure in audio that genre labels miss?

## Approach

We extracted acoustic features (MFCCs, spectral contrast, harmonic features) from the GTZAN dataset using **Librosa**, reduced dimensionality with **PCA**, then clustered with **K-Means**. Results were exposed through an interactive **Streamlit** app, containerised with Docker for reproducible deployment.

## Demo

The app is preserved as a demo of what we built: [kmeansklang.streamlit.app](https://kmeansklang.streamlit.app/)

> Note: the backend ran on GCP during the bootcamp. The frontend still loads and shows the interface, but full clustering won't run since we've sunset the cloud resources. See the screenshots below, or run it locally from the repo.

![Streamlit app](/projects/project-three/screenshot.png)

## Code

Full source and setup instructions: [github.com/zmokhtari89/k_means_klang](https://github.com/zmokhtari89/k_means_klang)

Team project (Le Wagon Data Science & AI Bootcamp, March 2025): Zahra Mokhtari, Eleni Kartsiouka, Tai Ford, Luisa Freytag.