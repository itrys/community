# ITrys 合规报告（Compliance Reports）

> **合规不是负担，是信任的证明。**

本目录存放 ITrys 入驻项目的合规认证报告。

---

## 报告类型

| 报告类型 | 文件格式 | 说明 |
|----------|----------|------|
| SBOM（软件物料清单） | SPDX JSON | 项目依赖与许可证清单 |
| 许可证扫描报告 | Markdown | 依赖许可证兼容性分析 |
| DCO 合规报告 | Markdown | 贡献者签名验证结果 |
| 综合合规报告 | Markdown | 入驻审核综合评估 |

---

## 目录结构

```
compliance-reports/
├── README.md                          # 本文件
├── projects/                          # 各项目合规报告
│   └── {project-name}/                # 以项目名命名的目录
│       ├── {project-name}-sbom.json   # SBOM 报告（SPDX 格式）
│       ├── {project-name}-license.md  # 许可证扫描报告
│       └── {project-name}-report.md   # 综合合规报告
└── templates/                         # 报告模板
    ├── sbom-template.json             # SBOM 模板
    ├── license-report-template.md     # 许可证报告模板
    └── compliance-report-template.md  # 综合报告模板
```

---

## 报告命名规范

| 文件 | 命名格式 | 示例 |
|------|----------|------|
| SBOM | `{project}-sbom-v{version}.json` | `itrys-cli-sbom-v1.2.0.json` |
| 许可证报告 | `{project}-license-{date}.md` | `itrys-cli-license-2026Q2.md` |
| 综合报告 | `{project}-report-{date}.md` | `itrys-cli-report-2026-04-13.md` |

> 日期格式：`YYYY-MM-DD` 或 `YYYYQN`（季度）

---

## 认证状态

入驻项目的认证状态可通过报告中的徽章标识：

| 状态 | 徽章 | 说明 |
|------|------|------|
| 孵化中 | `ITrys Incubating` | 已通过初审，进入孵化期 |
| 已认证 | `ITrys Certified` | 已通过完整合规审核 |
| 已过期 | — | 未按时更新合规报告 |

---

## 报告更新频率

| 项目状态 | SBOM | 许可证扫描 | 综合报告 |
|----------|------|------------|----------|
| 孵化期 | 每次版本发布 | 每月 | 入驻时 |
| 活跃期 | 每次版本发布 | 每季度 | 每年 |
| 归档 | 不更新 | 不更新 | 不更新 |

---

## 使用方式

### 项目维护者

1. 版本发布时运行 SBOM 生成工具
2. 将报告提交至本目录对应项目文件夹
3. 在项目 README 中添加认证徽章

### 社区用户

1. 查看目标项目的合规报告
2. 验证项目开源合规性
3. 用于企业安全审计

---

> **透明是信任的基石，每份报告都是一份承诺。**

---

*最后更新：2026-04-13*
