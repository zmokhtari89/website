+++
title = "Satellite Roof Segmentation"
description = "Binary semantic segmentation of rooftops from satellite imagery."
date = 2026-05-04
weight = 1

[extra]
thumbnail = "/projects/project-four/thumb.png"
tags = ["PyTorch", "Computer Vision", "Semantic Segmentation", "Transfer Learning"]
+++

## Problem

Given a satellite image of a residential area, predict a pixel-wise binary mask of rooftops, motivated by automated solar-panel planning.

The dataset is small (30 RGB images, 256×256, with 25 labelled masks and noisy annotations) and the train/val split leaves only 20 training images, making transfer learning essential.

## Approach

I trained four models: U-Net and U-Net++ (both with a ResNet34 encoder pretrained on ImageNet), each in two loss configurations: BCE + Dice (V1) and BCE + Dice with boundary weighting (V2). Models were selected on validation IoU and Dice.

## Results

The best model, **U-Net++ V1**, reached **IoU 0.82** and **Dice 0.90** on validation. Recall was prioritised over precision: in solar planning, missed roofs are missed installations, while false positives are filtered downstream.

![Predictions](/projects/project-four/predictions.png)

## Code

Full notebook, training code, and predictions: [github.com/zmokhtari89/roof_detection](https://github.com/zmokhtari89/roof_detection)