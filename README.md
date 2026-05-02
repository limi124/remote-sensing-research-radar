# Remote Sensing Research Radar

A Codex skill for tracking research frontiers in geospatial AI, remote sensing big data, and transferable computer vision methods.

This skill is designed for researchers who want to follow recent papers, open-source projects, datasets, benchmarks, and research trends in optical remote sensing and related computer vision fields. It explicitly avoids SAR-focused work by default, unless SAR is requested.

## Features

- Search and summarize recent remote sensing papers from arXiv, Papers with Code, GitHub, Hugging Face, conference pages, and benchmark pages.
- Track frontier topics in optical remote sensing, multispectral/hyperspectral imagery, geospatial big data, Earth observation foundation models, and multi-temporal learning.
- Include transferable computer vision methods such as foundation models, open-vocabulary segmentation, vision-language models, domain adaptation, OOD detection, weak supervision, and efficient inference.
- Filter out SAR, PolSAR, InSAR, radar-only, microwave-only, and SAR-optical fusion work by default.
- Rank candidate papers and projects by novelty, technical depth, evidence, reproducibility, trend signal, and transferability to remote sensing.
- Generate daily or weekly research radar reports.
- Produce related work tables, deep paper notes, reproducibility plans, and publishable research ideas.

## Research Scope

Recommended non-SAR directions:

- Earth observation foundation models
- Optical and multispectral remote sensing
- Hyperspectral image learning
- Multi-temporal satellite image modeling
- Optical change detection
- Remote sensing vision-language models
- Cross-region and cross-sensor generalization
- GIS/vector/raster fusion
- Large-scale efficient remote sensing inference
- Urban, agriculture, ecology, land-cover, and environmental monitoring applications

Transferable computer vision directions:

- Self-supervised learning and masked image modeling
- Vision transformers and foundation models
- Open-vocabulary segmentation and detection
- Vision-language models and visual grounding
- Video/temporal models for change reasoning
- Domain generalization and test-time adaptation
- Weakly supervised, semi-supervised, and active learning
- Efficient inference for large images

## Installation

Install this skill into your local Codex skills directory:

```powershell
python C:\Users\shuo\.codex\skills\.system\skill-installer\scripts\install-skill-from-github.py --repo <your-github-username>/<your-repo-name> --path skills/remote-sensing-research-radar
```

After installation, restart Codex so the skill can be discovered.

## Recommended Repository Structure

```text
your-repo/
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
帮我做本周地信遥感大数据前沿雷达，不要 SAR，重点关注遥感基础模型和多时相变化检测。
```

```text
用 remote-sensing-research-radar 找最近一个月值得读的遥感基础模型论文和开源项目。
```

```text
帮我追踪可迁移到遥感的计算机视觉论文，重点关注开放词汇分割、VLM 和 domain adaptation。
```

```text
基于最近的遥感和 CV 前沿，帮我提出 5 个可以冲高水平论文的选题。
```

## Output Format

Typical weekly radar output:

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

- The skill is optimized for Chinese research workflows, but paper titles and technical terms are preserved in English where appropriate.
- Web search should be used for fresh research reports, because arXiv, GitHub, Papers with Code, and conference pages change frequently.
- SAR-related research is excluded by default to match the intended research direction.
