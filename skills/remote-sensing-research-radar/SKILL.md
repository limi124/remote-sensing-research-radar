---
name: remote-sensing-research-radar
description: Track, retrieve, screen, and synthesize research frontiers for geospatial AI, remote sensing big data, and transferable computer vision methods. Use when Codex is asked to search recent papers, arXiv, GitHub projects, Papers with Code, datasets, benchmarks, competitions, or conference/workshop programs in remote sensing or CV methods that can inspire remote sensing; build daily/weekly research radar reports; compare papers; identify high-potential research directions; prepare related work; or propose publishable ideas. Default scope excludes SAR-focused work unless the user explicitly asks for SAR.
---

# Remote Sensing Research Radar

## Scope

Track optical remote sensing, multispectral/hyperspectral imagery, geospatial big data, Earth observation foundation models, multi-temporal learning, change detection, vision-language remote sensing, geospatial reasoning, urban/agriculture/ecology/disaster applications, transferable computer vision methods, and reproducible open-source projects.

Include computer vision work when it offers a credible path to remote sensing adaptation: foundation models, segmentation, detection, open-vocabulary recognition, vision-language models, self-supervised learning, video/temporal modeling, domain adaptation, robustness, OOD detection, efficient inference, or weak/semi-supervised learning. Always explain the transfer path from CV to remote sensing.

Default exclusion: do not prioritize SAR, PolSAR, InSAR, radar-only, microwave-only, or SAR-optical fusion work unless the user explicitly asks for it. If a source contains SAR among many topics, keep only non-SAR items or mark mixed-modality items as lower priority.

For detailed topic taxonomy, keyword sets, scoring rubrics, and output templates, read `references/frontier-radar.md` when producing a radar report or research plan.

## Workflow

1. Clarify or infer the research focus: task, sensor/data type, application, venue target, time window, and desired output depth.
2. Search current sources when freshness matters: arXiv, Papers with Code, GitHub, Hugging Face, conference/workshop programs, benchmark leaderboards, and dataset/competition pages.
3. Use query expansion from the reference file. Include both remote-sensing terms and general AI terms because high-impact methods often appear under computer vision or machine learning labels.
4. For CV results, require an explicit adaptation hypothesis for remote sensing data, tasks, or constraints before ranking them highly.
5. Filter results for relevance, freshness, reproducibility, and publishable potential. Exclude SAR-focused results by default.
6. Score candidates using novelty, technical depth, data/benchmark strength, code availability, trend signal, transferability to remote sensing, and fit to the user's stated direction.
7. Produce a compact synthesis first, then deeper notes for the top items.
8. Convert the frontier scan into actionable research ideas: baseline, gap, proposed method, datasets, evaluation metrics, risks, and target venues.

## Source Priorities

Use primary or near-primary sources whenever possible:

- Papers: arXiv pages, publisher pages, OpenReview, CVF, IEEE/ISPRS/ACM pages, author project pages.
- Code: official GitHub repositories before third-party reimplementations.
- Benchmarks: Papers with Code, official competition pages, EvalAI/Codalab pages, dataset homepages.
- Data/model hubs: Hugging Face papers/models/datasets, NASA/ESA/USGS/Microsoft/IBM/academic lab pages.

When using web results, cite links in the final answer. For claims about latest work, verify dates and prefer the most recent authoritative page.

## Report Modes

Use a mode based on the user request:

- Daily radar: 5-8 items from the last 1-3 days, concise trend notes.
- Weekly radar: 10-15 items from the last 7-14 days, ranked with scores and research ideas.
- Deep dive: 1-5 papers/projects, method and experiment analysis, limitations, reproducibility plan.
- Related work: grouped by problem family, with comparison table and narrative gaps.
- Topic discovery: broad scan that ends with 3-5 candidate thesis/paper directions.
- CV transfer scan: search recent computer vision work and rank only items with strong remote sensing adaptation potential.

## Output Rules

Prefer Chinese if the user writes Chinese. Keep English paper titles unchanged.

For radar reports, include:

- Executive summary: 3-5 bullets on frontier movement.
- Ranked table: title/project, source/date, task, data/modality, contribution, code/data status, score, why it matters.
- Top picks: 3 deeper analyses with method, experiments, limitations, and extension ideas.
- CV-to-RS transfer notes when CV papers are included: transferable component, required changes, likely remote sensing datasets, and risk.
- Research ideas: 3 concrete ideas with hypothesis, method sketch, datasets, metrics, baselines, risk.
- Reading queue: essential papers/projects to read next.

Avoid overclaiming. Distinguish verified source facts from inference. If search access is unavailable, state that the report is based on available local/user-provided material and ask for links or permission to search.
