# 遥感研究前沿雷达

[![Codex Skill](https://img.shields.io/badge/Codex-Skill-111827)](#)
[![Research Radar](https://img.shields.io/badge/Research-Frontier%20Radar-2563eb)](#)
[![Remote Sensing](https://img.shields.io/badge/Domain-Remote%20Sensing-059669)](#)
[![No SAR by Default](https://img.shields.io/badge/SAR-Excluded%20by%20Default-b91c1c)](#)

**语言:** [English](README.md) | 中文

这是一个用于追踪 **地信遥感大数据**、**Geospatial AI** 和 **可迁移计算机视觉方法** 的 Codex skill。

它面向科研场景，帮助研究者持续检索和汇总最新论文、开源项目、数据集、Benchmark、竞赛和会议前沿。默认聚焦光学遥感、地理空间智能和可迁移到遥感的计算机视觉方法。

> 默认排除 SAR、PolSAR、InSAR、雷达、微波、SAR-only 以及 SAR-optical fusion 方向，除非用户明确要求纳入 SAR。

## 为什么做这个 Skill

遥感研究的前沿并不只出现在遥感期刊里。很多重要方法会先出现在计算机视觉、机器学习、GIScience、Earth Observation 或 AI 顶会中，然后再迁移到卫星影像、航空影像和地理空间数据场景。

这个 skill 的目标就是把这些线索串起来：

| 需求 | Skill 能做什么 |
| --- | --- |
| 追踪新论文 | 检索 arXiv、Papers with Code、GitHub、Hugging Face、会议页面和 Benchmark 页面 |
| 借鉴 CV 前沿 | 筛选可迁移到遥感的计算机视觉论文和方法 |
| 避开无关方向 | 默认过滤 SAR 相关研究 |
| 建立阅读队列 | 按创新性、证据、可复现性和方向匹配度排序 |
| 形成选题 | 把前沿趋势转化为可投稿的研究 idea |
| 整理相关工作 | 生成 related work 表格和结构化文献综述 |

## 核心能力

- 每日或每周研究前沿雷达
- 论文与 GitHub 项目筛选
- 遥感基础模型与地信大数据方向追踪
- 计算机视觉到遥感的迁移分析
- Related work 对比表
- 深度论文阅读笔记
- 复现实验计划
- 可投稿选题生成

## 研究范围

### 遥感与地理空间智能

| 方向 | 示例主题 |
| --- | --- |
| 遥感基础模型 | MAE、JEPA、对比学习、掩码建模、地理位置/时间编码 |
| 光学与多光谱遥感 | Sentinel-2、Landsat、航空 RGB、无人机影像、超高分辨率场景理解 |
| 高光谱学习 | 光谱-空间建模、波段选择、跨域泛化 |
| 多时相建模 | 作物监测、土地覆盖变化、城市扩张、生态时间序列 |
| 变化检测 | 光学建筑物、土地覆盖、城市和生态变化检测 |
| 遥感视觉语言模型 | Captioning、VQA、Grounding、开放词汇分割 |
| 跨域泛化 | Domain adaptation、OOD 检测、小样本学习、空间偏差 |
| GIS 与栅格-矢量融合 | 道路、地块、POI、建筑轮廓、拓扑感知学习 |
| 大范围高效推理 | 切片、流式推理、压缩、主动学习、不确定性制图 |

### 可迁移计算机视觉方向

| CV 方向 | 迁移到遥感的路径 |
| --- | --- |
| Foundation models | 将通用视觉表征迁移到多光谱、高分辨率或多时相影像 |
| 开放词汇分割 | 支持灵活地物类别和区域化土地覆盖分类体系 |
| Vision-language models | 支持遥感 VQA、图像描述、视觉定位和检索 |
| 视频与时序模型 | 将长程时序建模迁移到卫星影像时间序列 |
| Domain adaptation | 提升跨城市、跨国家、跨季节、跨传感器泛化能力 |
| 弱监督/半监督学习 | 降低大范围遥感制图的标注成本 |
| 高效推理 | 面向大幅面遥感影像进行切片、压缩和流式推理 |

## 评分标准

候选论文和项目会按以下维度排序：

| 维度 | 含义 |
| --- | --- |
| 创新性 | 是否提出新问题、新方法、新 Benchmark 或新的问题重构 |
| 技术深度 | 是否有明确算法、模型或训练策略贡献 |
| 实验证据 | 数据集、指标、消融和泛化实验是否扎实 |
| 可复现性 | 是否有代码、数据、权重和清晰说明 |
| 趋势信号 | 是否来自活跃团队、热门项目、重要会议或 Benchmark |
| 迁移潜力 | CV/ML 方法是否能清楚迁移到遥感约束下 |
| 方向匹配 | 是否符合非 SAR 的地信遥感研究目标 |

## 安装方式

从本仓库安装 skill：

```powershell
python C:\Users\shuo\.codex\skills\.system\skill-installer\scripts\install-skill-from-github.py --repo limi124/remote-sensing-research-radar --path skills/remote-sensing-research-radar
```

安装后重启 Codex，让新 skill 生效。

## 推荐仓库结构

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

## 示例 Prompt

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

## 典型输出格式

```text
本周结论
- 趋势 1
- 趋势 2
- 趋势 3

候选论文/项目排行
| Rank | Title | Source/Date | Task | Data/Modality | Contribution | Code/Data | Score | Why it matters |

Top 3 深读
1. Title
   - 核心问题:
   - 方法:
   - 证据:
   - 局限:
   - 可延展方向:

CV-to-RS 迁移分析
- Paper/project:
- 可迁移组件:
- 需要适配的地方:
- 候选遥感数据集:
- 第一个实验:
- 风险:

可投稿研究选题
1. Idea name
   - Problem:
   - Hypothesis:
   - Method:
   - Datasets/Metrics:
   - Baselines:
   - First experiment:
```

## 注意事项

- 新论文、新项目和会议页面变化很快，生成前沿报告时应使用联网检索。
- 中文报告中也建议保留英文论文标题和关键技术术语，方便后续检索。
- 默认排除 SAR 方向，以保持和光学遥感、地信大数据、计算机视觉迁移研究目标一致。
