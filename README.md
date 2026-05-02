# Remote Sensing Research Radar

[![Codex Skill](https://img.shields.io/badge/Codex-Skill-111827)](#)
[![Research Radar](https://img.shields.io/badge/Research-Frontier%20Radar-2563eb)](#)
[![Remote Sensing](https://img.shields.io/badge/Domain-Remote%20Sensing-059669)](#)
[![No SAR by Default](https://img.shields.io/badge/SAR-Excluded%20by%20Default-b91c1c)](#)

**Language:** English | [中文](README.zh-CN.md)

A Codex skill for tracking research frontiers in **geospatial AI**, **remote sensing big data**, and **transferable computer vision methods**.

This project helps researchers continuously monitor new papers, open-source projects, datasets, benchmarks, and research trends. It focuses on optical remote sensing and geospatial AI, while also scanning computer vision methods that can be transferred into remote sensing research.

> SAR, PolSAR, InSAR, radar-only, microwave-only, and SAR-optical fusion work are excluded by default unless explicitly requested.

## Why This Skill

Remote sensing research moves quickly across multiple communities: geoscience, computer vision, machine learning, GIScience, and Earth observation. Important ideas often appear first in general CV or ML papers before being adapted to satellite and aerial imagery.

This skill is designed to bridge that gap:

| Need | What the skill does |
| --- | --- |
| Track new papers | Searches recent arXiv, Papers with Code, GitHub, Hugging Face, conference pages, and benchmark pages |
| Find useful CV methods | Screens computer vision papers for remote sensing transfer potential |
| Avoid noisy directions | Filters out SAR-focused work by default |
| Build a reading queue | Ranks papers and projects by novelty, evidence, reproducibility, and fit |
| Generate research ideas | Converts frontier trends into publishable research directions |
| Prepare related work | Produces comparison tables and structured literature summaries |

## Core Capabilities

- Daily or weekly research radar reports
- Paper and GitHub project screening
- Remote sensing frontier tracking
- Computer-vision-to-remote-sensing transfer analysis
- Related work table generation
- Deep paper reading notes
- Reproducibility planning
- Publishable idea generation

## Research Scope

### Remote Sensing and Geospatial AI

| Area | Example Topics |
| --- | --- |
| Earth observation foundation models | MAE, JEPA, contrastive learning, masked modeling, geolocation/time embeddings |
| Optical and multispectral imagery | Sentinel-2, Landsat, aerial RGB, UAV imagery, VHR scene understanding |
| Hyperspectral learning | Spectral-spatial modeling, band selection, domain generalization |
| Multi-temporal modeling | Crop monitoring, land-cover dynamics, urban expansion, ecological time series |
| Change detection | Optical building, land-cover, urban, and ecological change detection |
| Remote sensing VLMs | Captioning, VQA, grounding, open-vocabulary segmentation |
| Cross-domain generalization | Domain adaptation, OOD detection, few-shot learning, spatial bias |
| GIS and raster-vector fusion | Road networks, parcels, POIs, building footprints, topology-aware learning |
| Efficient inference | Tiling, streaming, compression, active learning, uncertainty-aware mapping |

### Transferable Computer Vision

| CV Direction | Remote Sensing Transfer Path |
| --- | --- |
| Foundation models | Adapt pretrained visual representations to multispectral, high-resolution, or multi-temporal imagery |
| Open-vocabulary segmentation | Map flexible land-cover classes and local taxonomy labels |
| Vision-language models | Support remote sensing VQA, captioning, grounding, and retrieval |
| Video and temporal models | Transfer long-range temporal reasoning to satellite image time series |
| Domain adaptation | Improve cross-city, cross-country, cross-season, and cross-sensor robustness |
| Weak/semi-supervised learning | Reduce annotation cost for large-scale mapping |
| Efficient inference | Handle large remote sensing images with tiled or compressed inference |

## Scoring Rubric

Candidate papers and projects are ranked by:

| Criterion | Meaning |
| --- | --- |
| Novelty | New problem, method, benchmark, or strong reframing |
| Technical depth | Clear algorithmic or modeling contribution |
| Evidence | Strong experiments, ablations, datasets, and metrics |
| Reproducibility | Code, data, weights, and clean instructions |
| Trend signal | Active authors, labs, stars, benchmarks, or conference attention |
| Transferability | Clear path from CV or ML to remote sensing constraints |
| User fit | Matches non-SAR geospatial remote sensing research goals |

## Installation

Install the skill from this repository:

```powershell
python C:\Users\shuo\.codex\skills\.system\skill-installer\scripts\install-skill-from-github.py --repo limi124/remote-sensing-research-radar --path skills/remote-sensing-research-radar
```

Restart Codex after installation so the skill can be discovered.

## Recommended Repository Structure

```text
remote-sensing-research-radar/
├─ README.md
├─ README.zh-CN.md
└─ skills/
   └─ remote-sensing-research-radar/
      ├─ SKILL.md
      ├─ agents/
      │  └─ openai.yaml
      └─ references/
         └─ frontier-radar.md
```

## Example Prompts

```text
Use remote-sensing-research-radar to find recent remote sensing foundation model papers and open-source projects from the past month. Exclude SAR.
```

```text
Build a weekly geospatial AI research radar. Focus on optical remote sensing, multi-temporal modeling, and transferable computer vision methods.
```

```text
Find computer vision papers on open-vocabulary segmentation, VLMs, and domain adaptation that could inspire remote sensing research.
```

```text
Based on recent remote sensing and CV frontiers, propose five publishable research ideas for a high-impact paper.
```

## Typical Output

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
```

## Notes

- Fresh research reports should use web search because arXiv, GitHub, Papers with Code, and conference pages change frequently.
- English paper titles and technical terms should be preserved even in Chinese reports.
- SAR-related work is excluded by default to keep the radar aligned with optical remote sensing and geospatial AI research.
