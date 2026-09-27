---
layout: page
title: "Augmented tissue histopathology evaluation and navigation assistant for digital pathology"
description: "Poster Presentation · Pathology Visions 2026 · San Diego, CA · October 16–18, 2026"
importance: 1
category: Posters
---

---

### Presentation Details

- **Type**: Poster Presentation
- **Conference**: Pathology Visions 2026
- **Location**: San Diego, CA
- **Date**: October 16–18, 2026

### Abstract

**Introduction**  
Modern spatial omics assays are powerful but constrained by cost and capture area, limiting large-scale analysis. Histopathologic review of hematoxylin and eosin (H&E) slides offers a cost-effective, high-resolution alternative for large-scale tissue characterization. We present ATHENA, an integrated computational pipeline that uses routine H&E images to support tissue characterization, expert annotation, and region-of-interest (ROI) selection for downstream molecular analysis.

**Methods**  
ATHENA integrates three components for whole-slide image analysis. A cell-resolution segmentation module is designed to operate efficiently on large images despite memory and GPU constraints, enabling rapid characterization of tissue architecture across diverse cohorts. A human-in-the-loop label propagation module extends sparse expert annotations and directs specialist review toward rare cell types and transitional states. A navigation module identifies representative regions for expert review, reducing the manual burden of pathology annotation.

**Results**  
ATHENA refined coarse manual annotations commonly generated in research workflow and spot-level annotations that are crucial for identifying cell types involved in cell-cell interactions and tumor microenvironment. Within individual samples, ATHENA propagated labels from a small number of expert examples and detected scattered structures such as microvascular proliferation in glioblastoma. These outputs support downstream tasks including pathology scoring and ROI selection by improving consistency of tissue review and helping prioritize regions that capture histologic heterogeneity.

**Conclusion**  
By combining scalable segmentation, expert-guided label refinement, and intelligent navigation, ATHENA links routine morphology with downstream molecular assays. This framework supports more standardized and reproducible tissue review and facilitates morphology-informed experimental design.
