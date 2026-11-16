---
layout: page
title: Projects
permalink: /projects/
---

## Commerce POS application
We are transforming how orgnanizations build software products in the world of AI.

## PredictSpring Modern POS
We build the most amazing point of sales terminal. It is currently used on 15 countries and 3 continents by major brands.

## Exploring Visual Product Identification for Retail
Can a photograph identify a product in a merchant's existing catalog accurately enough to help a store associate? This prototype explores visual catalog matching for retail tasks such as looking up an item without a readable label, identifying a return, and reconciling physical merchandise with catalog records.

The first implementation is a command-line tool built with TensorFlow and Keras. It uses a frozen pretrained DINOv2 model to extract image embeddings and compare them with catalog reference images, returning ranked product style candidates while preserving their size and color variant mappings.

Early catalog analysis showed why the data model matters: 273 product IDs in one catalog mapped to only 13 style groups, with many IDs representing variants rather than visually distinct designs. It also exposed a key limitation of whole-image similarity: separate jersey and shorts records can share the same photo of a model wearing both garments. Reference composition, the intended object, and catalog relationships are therefore part of the recognition problem.

The pipeline is working, but retrieval against an image's own reference does not establish accuracy for store photography. Next, I will evaluate independent images, similar-looking products, and out-of-catalog items, measuring retrieval accuracy, incorrect matches, review effort, and latency. The goal is to determine where visual identification is useful, where additional evidence is necessary, and whether it makes a real retail task easier.
