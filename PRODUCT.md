# Product

<!-- impeccable:product-schema 1 -->

## Platform

web

## Stack

Static HTML/CSS/JS, single page, three.js loaded from a CDN. No build step. Deployed from a public GitHub repo to Netlify.

## Users

A civil engineering student and their lab group (Pavimentos, semestre 2026-II). They study the night before the lab and keep the page open on a phone during the session: mixing and compacting on Saturday 10 Oct 2026, breaking the specimens on Tuesday.

## Product Purpose

A study guide for the INVIAS test standard INV E-748-13 (estabilidad y flujo de mezclas asfálticas en caliente, equipo Marshall). Success: the group understands the goal of the test, can follow the procedure step by step with its numbers (temperatures, times, blows, load rate), and knows how to compute and report stability and flow.

## Positioning

Built from the standard itself, page by page, and mapped to this group's actual lab schedule, including where that schedule departs from the standard (6.1 asks for testing within 24 h of compaction; the group tests about 72 h later).

## Operating Context

Read on a laptop while studying and on a phone in the lab, possibly with gloves and hot equipment around. Aggregates are already dried, sieved and weighed. Method A (load ring and dial gauge) is the likely setup but not confirmed.

## Capabilities and Constraints

- Content in Spanish.
- Every number must come from INV E-748-13. Anything not in the standard (ring calibration constant, example calculation) is labeled as such.
- Number of blows per face is not fixed by the standard; confirm with the professor.
- The standard PDF itself is not republished.

## Evidence on Hand

- `INV E-748-13 ... MARSHALL.pdf` (20 pages) in this folder: the only source.
- Previous version of the guide: `Guia_estudio_Marshall_INV_E-748.html`.

## Product Principles

1. The procedure in the right order, with its numbers, beats prose.
2. Usable one-handed on a phone in the lab.
3. Mark clearly what the standard says versus what the lab decides.
