---
title: "Processing needs"
author: "Lukas Kluft"
format:
  revealjs:
    transition: slide
    slide-number: true
    code-background: true
    logo: /static/logos.png
    footer: "[Talks page](/talks)"
    theme: [default, ../custom.scss]
    chalkboard:
      buttons: true
    navigation-mode: linear
    auto-stretch: true
    center: true
    mermaid:
      theme: default
---

## Hardware

* a couple of dedicated nodes in a SLURM partition (~32 at DKRZ)
* limit of **2 nodes per participant** (larger jobs are usually user error)

## Services

* Jupyterhub (or similar) is usually an appreciated entry point

## Python environments

* it's hard (if not impossible) to provide a single environment for all users
* _Compromise:_ provide a lean python environment with packages available through `mambaforge`
* users can install their exotic dependencies on top of that
* Make sure to use the *forge* version of conda things to avoid license issues.[^1]

[^1]: [prefix.dev blog post](https://prefix.dev/blog/towards_a_vendor_lock_in_free_conda_experience)
## Data

* test access of data **using the hackathon environment**
