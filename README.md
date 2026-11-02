# study-skill

A reusable, privacy-conscious workspace for gastric cancer research, systematic reviews/meta-analyses, Mendelian randomization (MR), and NHANES analyses.

这是一个可复用、重视隐私保护的科研项目管理工作区，初始覆盖胃癌临床研究、系统综述与 Meta 分析、孟德尔随机化（MR）及 NHANES 分析。

> This repository contains structure and templates only. It does not contain patient data, research results, or fabricated example data.
>
> 本仓库仅包含目录结构与模板，不包含患者数据、研究结果或虚构示例数据。

## Workspace layout / 工作区结构

```text
.
├── research-protocols/     # Research protocols / 研究方案
├── literature-screening/  # Search and screening records / 文献检索与筛选
├── data-dictionaries/     # Variable definitions / 数据字典
├── analysis-scripts/      # Reproducible code / 可复现分析脚本
├── outputs/               # Reviewed, non-sensitive outputs / 经审查的非敏感结果
├── CHANGELOG.md           # Change history / 变更记录
├── VERSIONING.md          # Versioning rules / 版本规则
└── PRIVACY.md             # Privacy policy / 数据隐私规范
```

Each research area includes a README so its intended use remains visible before project files are added.

## Supported areas / 初始研究方向

- **Gastric cancer clinical research / 胃癌临床研究:** protocols, controlled variable definitions, and reproducible clinical analyses.
- **Systematic review and meta-analysis / 系统综述与 Meta 分析:** search strategies, screening logs, extraction definitions, and synthesis scripts.
- **Mendelian randomization / 孟德尔随机化:** source documentation, instrument selection, harmonization, sensitivity analyses, and reporting.
- **NHANES:** cycle documentation, variable mapping, eligibility, complex survey design, weighting, and disclosure-aware reporting.

## Recommended workflow / 建议流程

1. Copy [the protocol template](research-protocols/protocol-template.md) into the relevant project folder and complete it before analysis.
2. Record searches and decisions with [the screening log template](literature-screening/screening-log-template.csv).
3. Define variables and provenance with [the data dictionary template](data-dictionaries/data-dictionary-template.csv).
4. Copy [the analysis README template](analysis-scripts/analysis-readme-template.md) into a new analysis folder.
5. Document every result set with [the result record template](outputs/result-record-template.md), then complete privacy and disclosure review before committing outputs.
6. Update [the changelog](CHANGELOG.md) and follow [the versioning rules](VERSIONING.md).

## Privacy first / 隐私优先

Never commit identifiable patient information, raw medical records, credentials or keys, or restricted/licensed data. Keep local data outside version control and commit only approved, non-identifying code, documentation, metadata, and disclosure-reviewed outputs. Read [the privacy policy](PRIVACY.md) before adding any data-derived file.

严禁提交可识别患者身份的信息、原始病历、账号密钥以及受限或授权数据。所有本地数据应置于版本控制之外；仅可提交经过批准且不含身份信息的代码、文档、元数据和通过披露审查的结果。添加任何数据衍生文件前，请先阅读[数据隐私规范](PRIVACY.md)。

## Starting a project / 新建项目

Use one short, stable project slug (for example, `gc-survival-2026`) across protocols, screening, dictionaries, scripts, and output records. Never use patient identifiers in paths, filenames, branches, commits, or issues.

Keep commits focused, document analysis decisions, and never use Git history as sensitive-data storage. If sensitive information is committed accidentally, stop sharing the repository and follow the incident steps in [PRIVACY.md](PRIVACY.md).
