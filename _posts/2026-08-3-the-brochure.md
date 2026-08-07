---
title: The Brochure | TryHackMe Challenge
date: 2026-08-06 3:20:00 +0000
categories: [CTF]
tags: [tryhackme, osint]
author: Abdelrahim Nabil
image:
  path: /assets/img/posts/the-brochure/header.png
  alt: The Brochure TryHackMe challenge
---

## quick intro

**The Brochure** is an OSINT challenge from TryHackMe that focuses on following digital clues across social media.

The challenge description states:

> The brochure’s hero photo has an **AI fingerprint**. Follow the account that posted it, and the trail doesn’t **end at the hotel**; it ends at someone the hotel **never mentioned**.
>
> Follow the trail, uncover the **hidden connection**, and find what was left behind.

---

## Downloading the Challenge Image

The first step was downloading the provided image.

![Byte Lotus Resort Task Image](/assets/img/posts/the-brochure/task-image.png)

---

## Inspecting Image Metadata

Whenever I receive an image during an OSINT challenge, I like to begin by checking its metadata.

```bash
exiftool thebrochure.png
```

Unfortunately, there was nothing particularly interesting hidden inside the metadata.

![ExifTool Result](/assets/img/posts/the-brochure/exif.png)

---

## Looking at the Visible Clues

Since the metadata didn't reveal anything useful, I focused on the information visible inside the image itself.

The brochure already provided several clues:

- Hotel name 
- Date
- Social media platform
- The name **"VERA"**

The name **VERA** immediately caught my attention because it appeared in another challenge as the AI assistant's name.

I decided to search Google for the hotel's Instagram account.

Searching for:

```
@bytelotusresorts
```
![Byte Lotus Resort Google](/assets/img/posts/the-brochure/gsearch.png)

quickly led me to the correct Instagram profile.

![Byte Lotus Resort Instagram](/assets/img/posts/the-brochure/instagram.png)

At first, I thought that would be enough...

But it wasn't.

![thinking](/assets/img/posts/the-brochure/cat.png)

---

## Inspecting the Posts

I opened each Instagram post and zoomed in carefully, expecting the flag to be hidden somewhere inside the images.

### First Post

![First Post](/assets/img/posts/the-brochure/post1.png)

### Second Post

![Second Post](/assets/img/posts/the-brochure/post2.png)

Unfortunately, I couldn't find anything.

I also checked the account bio and About section, but there was still nothing useful.

---

## A Suspicious Detail

Then something caught my eye.

The hotel account was following **only one account**.
![Vera](/assets/img/posts/the-brochure/follow1.png)

That seemed very intentional.

The account was...
**VERA**

Exactly the same name mentioned in the challenge image.
![Vera](/assets/img/posts/the-brochure/vera.png)

![Vera](/assets/img/posts/the-brochure/vera2.png)

---

## Following the Trail

After opening VERA's profile, I immediately noticed something unusual.

There were three posts, each containing what looked like encoded text.

### First Part

![First Part](/assets/img/posts/the-brochure/vera-post1.png)

### Second Part

![Second Part](/assets/img/posts/the-brochure/vera-post2.png)

### Third Part

![Third Part](/assets/img/posts/the-brochure/vera-post3.png)

The strings looked very similar to **Base64** encoding.

---

## Decoding the Messages

After copying all three parts together, I decoded the Base64 string.


The decoded message revealed the challenge flag.

![Base64 Decoding](/assets/img/posts/the-brochure/base64-decode.png)

---

## Flag
![flag](/assets/img/posts/the-brochure/flag.png)

> **THM{V3r@s_aCC0unt_h4s_b33n_f0und!}**

---

## Completed
![Base64 Decoding](/assets/img/posts/the-brochure/finish.png)


