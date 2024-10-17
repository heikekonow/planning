---
title: "Storage requirements"
author: "Florian Ziemen"
subtitle: ""
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

# Storage requirements

## Ballpark estimate for level 9 (13km)

| type | cells / snapshot | snapshots | GB / var [^1] | vars requested | GB total| 
|------|------|---------|-------|------|-----|
| 2D   | 3 M     | 365*24    | 52      |  30 | 1500 |
| 2D[^2]   | 3 M     | 365*4    | 13      |  30 | 250 |
| 3D   |75 M | 365*4 | 220 |12 | 2600|


[^1]: Assuming 50% compression
[^2]: For consistent datasets

## Making things useful


* Adding the full healpix hierarchy adds 30%, and makes the dataset useful.
* Add daily means (+25% w.r.t the 6-hourly data)
* Total size per dataset at 13 km: 6.6TB
* Doubling the resolution multiplies the storage need by 4.