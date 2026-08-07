---
title: Find The Masked Man | OSINT Industires CTF
date: 2026-07-19 3:20:00 +0000
categories: [CTF]
tags: [Osint Industries, osint]
author: Abdelrahim Nabil
image:
  path: /assets/img/posts/find-the-masked-man/header.webp
  alt: Find The Masked Man!
---

## What is Find The Masked Man CTF talking about ?

> A photograph was taken in **Paris on December 3rd**, **2023, around 18:00**.
> Your mission is to **identify the nearest metro station** to the location where the masked man was photographed.

> **Investigators** received an image showing a **masked individual** standing in a **central and upscale district of Paris**.
> The metadata and environmental observations indicate:

- The image was taken on **December 3rd**, 2023
- The approximate time was **18:00** (early evening)
- The location is in **Paris**, within a **central and upscale area**
- The scene is located near the intersection of a **Rue** and **an Avenue**


---

## Your Objective

- Analyze the given information and identify the nearest Paris metro station.
- The Flag should be like this format OSINT{STATION_NAME}

---

## Inspecting The Image



![Masked Man](/assets/img/posts/find-the-masked-man/masked.webp)

![Zoomed In Masked Man](/assets/img/posts/find-the-masked-man/zoomed-in-masked.webp)


This is the only Image provided so, I zoomed the Image in.

It appears to be a Restaurant and have an Ad Banner in front of it therefore I wrote to the note

- Restaurant name “ **JULIEN** ”
I have tried to quick search for “**Rue Avenue Paris Julien restaurant**”

![Rue Avenue Paris Julien restaurant](/assets/img/posts/find-the-masked-man/first-search.webp)


and found that the AI Suggests Two Restaurants So I Clicked on the first one

![Bouillon Julien](/assets/img/posts/find-the-masked-man/second-search.webp)

And it wasn’t the restaurant in the masked man picture and not the same street so, I clicked on the second one

![Chez Julien](/assets/img/posts/find-the-masked-man/third-search.webp)
![Chez Julien](/assets/img/posts/find-the-masked-man/third-search2.webp)

At the first look you might think that this was the restaurant but no, wasn’t the same

*So I searched with this **Google Dork** with the information provided before, wish find the correct one now.*
```
"Julien" "Paris" (intersection OR corner) ("avenue" AND "rue")
```
![Google Dork Search](/assets/img/posts/find-the-masked-man/forth-search.webp)

And I found another Restaurant Called “ **MAISON JULIEN** ” on *TripAdvisor* so I opened it !
![MAISON JULIEN](/assets/img/posts/find-the-masked-man/trip.webp)
![MAISON JULIEN](/assets/img/posts/find-the-masked-man/trip2.webp)

> See the same Restaurant and the same Ad banner I will add the CTF image to make you recognize it.
![Masked Man](/assets/img/posts/find-the-masked-man/masked.webp)

Now I know the **Restaurant** But I have to get the **nearest metro station**
[![MAISON JULIEN on Google Maps](/assets/img/posts/find-the-masked-man/metro.webp)](https://maps.app.goo.gl/oRonpoGvDWkQPUGVA)

[![MAISON JULIEN on Google Maps](/assets/img/posts/find-the-masked-man/metro2.webp)](https://maps.app.goo.gl/oRonpoGvDWkQPUGVA)



And I Found the Nearest Metro Station name is [ <u>*Saint-Philippe-du-Roule*</u> ]

> So The FLAG Is = **OSINT{SAINT_PHILIPPE_DU_ROULE}**


![](/assets/img/posts/find-the-masked-man/finish.webp)
