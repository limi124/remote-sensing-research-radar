# Frontier Radar Reference

## Default Topic Taxonomy

Prioritize these non-SAR directions for geospatial AI and remote sensing big data:

1. Earth observation foundation models: MAE, JEPA, contrastive learning, masked modeling, multi-temporal pretraining, geolocation/time embeddings, any-resolution adaptation.
2. Optical and multispectral remote sensing: Sentinel-2, Landsat, NAIP, Planet-style imagery, aerial RGB, UAV imagery, very-high-resolution scene understanding.
3. Hyperspectral learning: spectral-spatial modeling, band selection, spectral foundation models, domain generalization.
4. Multi-temporal learning: crop monitoring, land-cover dynamics, urban expansion, phenology, climate/ecology time series, long-context temporal modeling.
5. Change detection: building/land-cover/urban/ecological change using optical or multispectral time series; avoid SAR-only change detection unless requested.
6. Remote sensing vision-language models: captioning, VQA, text-grounded retrieval, open-vocabulary segmentation/detection, geospatial instruction tuning.
7. Cross-region and cross-sensor generalization: domain adaptation, test-time adaptation, OOD detection, few-shot/low-label learning, spatial bias and fairness.
8. Geospatial reasoning and GIS fusion: raster-vector fusion, map priors, POI/road/building footprints, topology, spatial autocorrelation, coordinate-aware models.
9. Large-scale efficient inference: tiling, streaming, compression, embeddings, active learning, weak supervision, uncertainty-aware mapping.
10. Applications: land cover/use, agriculture, urban analytics, ecology/biodiversity, disaster assessment from optical imagery, environmental monitoring, public health and socioeconomic mapping.

## Transferable Computer Vision Topics

Track CV work when it can plausibly transfer to remote sensing:

1. Foundation models and representation learning: DINO, MAE, JEPA, CLIP-style contrastive learning, masked image modeling, any-resolution encoders.
2. Segmentation and detection: semantic/instance/panoptic segmentation, small object detection, dense prediction, promptable segmentation, open-vocabulary detection.
3. Vision-language models: image-text alignment, VQA, captioning, grounding, referring segmentation, multimodal instruction tuning.
4. Temporal and video learning: long-range temporal modeling, memory models, event detection, change reasoning, video foundation models.
5. Domain generalization and robustness: OOD detection, test-time adaptation, distribution shift, calibration, uncertainty, spurious correlation mitigation.
6. Data-efficient learning: weak supervision, semi-supervised learning, active learning, synthetic data, label noise robustness.
7. Efficient large-scale inference: token pruning, distillation, feature compression, tiled inference, streaming inference, retrieval-augmented vision.
8. Geometric and spatial reasoning: equivariance, topology-aware learning, graph neural networks, neural fields, scene graphs, spatial relation reasoning.

For each CV candidate, write a CV-to-RS transfer note:

- Transferable component: model, loss, training recipe, benchmark protocol, or evaluation idea.
- Required adaptation: multispectral channels, georeferencing, large images, scale variation, temporal stacks, sparse/noisy labels, spatial autocorrelation.
- Candidate RS task: land cover mapping, change detection, object detection, crop/urban/ecology monitoring, VQA, open-vocabulary mapping.
- First validation: smallest public remote sensing dataset and metric that can test the transfer.
- Risk: remote sensing data mismatch, compute cost, lack of labels, weak novelty, or method already tried in RS.

## Exclusion and Downranking

Exclude or downrank by default:

- SAR, PolSAR, InSAR, radar, microwave, interferometry, coherence, backscatter, speckle, SAR-optical fusion.
- Pure remote sensing hardware/calibration papers without a machine learning or geospatial big-data angle.
- Generic CV papers with no credible path to geospatial data unless the method is highly transferable.
- Projects without paper, code, data, or clear methodological novelty unless they signal a major trend.

If a high-value paper mixes SAR with optical/multispectral, include it only when its contribution is modality-agnostic or useful without SAR. Mark modality risk explicitly.

## Query Expansion

Core search phrases:

- remote sensing foundation model
- earth observation foundation model
- geospatial foundation model
- satellite image foundation model
- multispectral self-supervised learning
- optical remote sensing semantic segmentation
- remote sensing change detection optical
- multi-temporal satellite image learning
- remote sensing vision language model
- geospatial vision language model
- open vocabulary remote sensing segmentation
- remote sensing domain adaptation
- remote sensing out-of-distribution detection
- geospatial big data deep learning
- land cover mapping foundation model
- urban remote sensing deep learning
- crop monitoring satellite deep learning
- hyperspectral foundation model

Computer vision transfer search phrases:

- computer vision foundation model remote sensing transfer
- open vocabulary segmentation remote sensing
- vision language model remote sensing transfer
- promptable segmentation satellite imagery
- test time adaptation semantic segmentation remote sensing
- domain generalization dense prediction remote sensing
- self supervised vision transformer satellite imagery
- small object detection aerial imagery transformer
- video foundation model change detection remote sensing
- weakly supervised semantic segmentation remote sensing
- active learning remote sensing segmentation
- efficient vision transformer large image inference
- panoptic segmentation aerial imagery
- visual grounding remote sensing image

Negative terms for search refinement when needed:

- SAR
- PolSAR
- InSAR
- radar
- microwave
- speckle
- coherence
- interferometric

Source-specific query examples:

- arXiv: `remote sensing foundation model site:arxiv.org`
- GitHub: `remote sensing foundation model GitHub`
- Papers with Code: `remote sensing semantic segmentation Papers with Code`
- Conference: `CVPR EarthVision remote sensing foundation model 2026`
- Dataset: `remote sensing land cover dataset multispectral benchmark`

## Scoring Rubric

Score each item from 0-10:

- Novelty: new problem, new method, or strong reframing.
- Technical depth: clear model/algorithm contribution beyond engineering assembly.
- Evidence: convincing datasets, metrics, ablations, generalization tests.
- Reproducibility: code/data/model weights available, clean instructions, standard benchmarks.
- Trend signal: strong authors/labs, fast GitHub stars, benchmark activity, workshop/competition relevance.
- Transferability: clear path from CV method to remote sensing data constraints and benchmarks.
- User fit: matches the user's non-SAR geospatial remote sensing direction and target venue.

Interpretation:

- 9-10: read immediately; possible research anchor.
- 7-8: strong candidate; compare with nearby work.
- 5-6: useful background or baseline.
- below 5: mention only if it fills a gap.

## Research Idea Template

For each proposed idea, include:

- Problem: the unresolved gap.
- Hypothesis: the testable claim.
- Method sketch: model/data/training/evaluation plan.
- Datasets: likely public datasets or how to construct data.
- Baselines: recent foundation models, task models, classical geospatial methods if relevant.
- Metrics: task metrics plus generalization/efficiency/uncertainty metrics when appropriate.
- Expected contribution: why this could be publishable.
- Risk: data access, compute, weak novelty, annotation noise, domain shift.
- First experiment: the smallest experiment that can falsify or support the idea.

## CV-to-RS Idea Patterns

Use these patterns to convert CV frontiers into remote sensing ideas:

- Replace RGB assumptions with multispectral or hyperspectral input while preserving pretrained knowledge.
- Convert image-level VLM capabilities into pixel-level or object-level geospatial grounding.
- Adapt open-vocabulary segmentation/detection to land-cover classes and local map taxonomies.
- Turn video temporal models into multi-temporal satellite change reasoning.
- Use domain generalization methods to test cross-city, cross-country, cross-season, or cross-sensor robustness.
- Use uncertainty and calibration methods for trustworthy large-scale mapping.
- Combine CV foundation features with GIS vector priors such as roads, parcels, POIs, building footprints, or administrative boundaries.

## Output Template

Use this structure for a weekly radar:

```text
Weekly takeaways
- Trend 1
- Trend 2
- Trend 3

Ranked candidates
| Rank | Title | Source/Date | Task | Data/Modality | Contribution | Code/Data | Score | Why it matters |

Top 3 deep dives
1. Title
   - Core problem:
   - Method:
   - Evidence:
   - Limitations:
   - Extension:

CV-to-RS transfer notes
- Paper/project:
- Transferable component:
- Required adaptation:
- Candidate RS datasets:
- First experiment:
- Risk:

Publishable research ideas
1. Idea name
   - Problem:
   - Hypothesis:
   - Method:
   - Datasets/Metrics:
   - Baselines:
   - First experiment:

Next reading queue
- Paper/project 1
- Paper/project 2
```

For related work, group by method families rather than by chronology unless the user asks for historical development.
