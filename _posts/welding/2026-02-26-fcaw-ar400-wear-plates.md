---
layout: article
title: "FCAW on AR400 Wear Plates — Field Notes from a Mining Fabrication Shop"
description: "How I approach flux-cored arc welding on AR400 abrasion-resistant steel in a mining fabrication context. Preheat, wire selection, interpass temperature, and lessons learned."
date: 2026-02-26
category: welding
permalink: /blog/welding/fcaw-ar400-wear-plates/
image: /images/blog/fcaw-ar400-wear-plates.webp
image_alt: "FCAW welding on AR400 abrasion-resistant steel"
read_time: 8
tags:
  - FCAW
  - AR400
  - mining
  - wear plates
  - welding procedure

faq:
  - q: "What wire do you use for welding AR400 steel?"
    a: "I use E71T-1C flux-cored wire for most AR400 applications in mining fabrication. It handles the high-carbon content well and provides good impact toughness in the weld metal."
  - q: "What preheat temperature is required for AR400?"
    a: "For AR400 up to 25mm thickness, I preheat to a minimum of 100°C (210°F). Above 25mm, I go to 150°C (300°F) minimum and monitor interpass temperature throughout."
  - q: "Can you weld AR400 with SMAW stick welding?"
    a: "Yes, SMAW works for AR400 using low-hydrogen electrodes like E7018. It's slower than FCAW but gives you more control in tight positions or field repairs."

howto:
  name: "How to weld AR400 wear plates with FCAW"
  description: "Step-by-step process for flux-cored arc welding on AR400 abrasion-resistant steel in a fabrication shop environment."
  steps:
    - name: "Verify base metal certification"
      text: "Check the mill cert for carbon equivalent (CE). AR400 typically runs CE around 0.55–0.65. This drives your preheat requirement."
    - name: "Preheat to minimum temperature"
      text: "Use a calibrated temp stick or infrared thermometer. For AR400 under 25mm, minimum 100°C. Heat evenly, 75mm each side of the joint."
    - name: "Set up your FCAW parameters"
      text: "For E71T-1C on AR400, I run 23–25V and 220–250A on flat/horizontal. Drag angle 10–15 degrees. CO2 shielding at 18–20 L/min."
    - name: "Monitor interpass temperature"
      text: "Do not exceed 250°C interpass on AR400. Higher temperatures reduce the hardness of the base metal in the heat-affected zone."
    - name: "Slow cool after welding"
      text: "Cover the assembly with welding blankets immediately after completion. No quenching with water. Slow cooling prevents hydrogen cracking."
---

AR400 is one of those materials that separates the welders who read procedures from the ones who actually understand why the procedures exist.

It's abrasion-resistant steel — hardened to around 400 Brinell — and it will crack on you if you treat it like mild steel. I've seen it happen. You skip preheat, you rush the cooling, and 48 hours later you've got a cold crack running straight through your weld. The part is scrap, the timeline is blown, and everyone is looking for someone to blame.

This is what I've learned from doing it right, and occasionally seeing others do it wrong.

## Why AR400 Requires a Different Approach

The hardness that makes AR400 so useful in mining applications — conveyor buckets, chute liners, screen panels — comes from its microstructure. High carbon, alloying elements, quench and temper process. That same microstructure is what makes it sensitive to heat input.

When you weld it, you create a heat-affected zone (HAZ) where the base metal gets briefly heated above its transformation temperature and then cools. If it cools too fast — which it will if you skip preheat in a cold shop — you get martensite formation and potential hydrogen cracking.

The carbon equivalent on AR400 typically runs around 0.55 to 0.65. That number tells you everything you need to know about preheat requirements.

## Wire Selection

For FCAW on AR400 in a shop environment, I use **E71T-1C** as my default. A few reasons :

- Good impact toughness in the deposited weld metal
- Works well with CO2 shielding which I run at 18–20 L/min
- Forgiving on fit-up variations which are common in worn mining equipment repairs

For critical structural welds where toughness requirements are specified in the WPS, I'll switch to a low-hydrogen wire with better CVN values. Always check the WPS first.

## Parameters

On flat and horizontal positions :

- Voltage : 23–25V
- Amperage : 220–250A
- Travel speed : steady, consistent — AR400 doesn't like erratic heat input
- Drag angle : 10–15 degrees

These are starting points. Your specific wire diameter, contact-tip-to-work distance, and shop conditions will move these numbers. Run test coupons before touching the production parts.

## The Interpass Temperature Rule

**Do not exceed 250°C interpass on AR400.**

This is the one that trips people up on multi-pass welds. You get into a rhythm, the metal is warm, you're making good progress — and you've been running 300°C interpass for the last hour. You've just softened the HAZ and reduced the wear resistance of the base metal right next to your weld.

Use a contact thermometer or calibrated temp sticks. Check before every pass. It takes 30 seconds.

## Post-Weld

Cover immediately with welding blankets. The goal is to slow the cooling rate and allow hydrogen to diffuse out of the weld metal. No fans, no open doors, no water.

If you're in a heated shop at 20°C, you'll be fine with blankets for 2–3 hours. If you're in a cold environment — and in Quebec City in January, cold is relative — extend that time and consider a post-heat at 150°C for an hour.

---

This is the baseline. Every AR400 job has its own variables — thickness, joint configuration, filler requirement, code compliance. But if you get the preheat right, the interpass right, and the cooling right, you'll get sound welds every time.
