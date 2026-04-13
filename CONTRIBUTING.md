# ITrys 贡献指南（Contributing Guide）

> **我们不要求你"完美"，只要求你"真诚尝试"。**

感谢你对 ITrys 的关注！无论你是写代码、写文档、提建议，还是帮忙测试，你的贡献都至关重要。

---

## 1. 快速开始

### 1.1 找到适合你的方式

| 角色 | 适合人群 | 起步方式 |
|------|----------|----------|
| 🌱 **贡献者** | 所有人 | 从 `good-first-issue` 开始 |
| 💡 **项目发起人** | 有项目想法的人 | 提交 RFC 提案 |
| 🤝 **合作伙伴** | 企业、高校、组织 | 联系 contact@itrys.org |

### 1.2 基本流程

```
Fork → Clone → Branch → Commit → Push → PR → Review → Merge
```

---

## 2. 贡献类型

### 2.1 代码贡献

1. 在目标仓库找到标有 `good-first-issue` 或 `help-wanted` 的 Issue
2. 在 Issue 中评论表示你将处理该问题
3. Fork 仓库并创建分支：`fix/issue-123` 或 `feat/new-feature`
4. 编写代码，确保通过测试
5. 提交 PR，关联对应 Issue

### 2.2 文档贡献

- 修复拼写/语法错误：直接提交 PR
- 新增/重写文档：先创建 Issue 讨论范围
- 翻译文档：遵循项目现有翻译规范

### 2.3 Issue 报告

好的 Bug 报告应包含：

```markdown
## 问题描述
简要描述遇到的问题

## 复现步骤
1. ...
2. ...
3. ...

## 期望行为
描述你期望发生什么

## 实际行为
描述实际发生了什么

## 环境信息
- 操作系统：
- 软件版本：
- 其他相关信息：

## 补充信息
截图、日志等
```

### 2.4 代码审查

- 尊重提交者，提供建设性反馈
- 关注代码逻辑、安全性和可维护性
- 使用约定俗成的审查标签：
  - `nit:` — 小问题（非阻塞）
  - `suggestion:` — 建议改进
  - `question:` — 需要澄清
  - `issue:` — 必须修改（阻塞合并）

---

## 3. 分支与提交规范

### 3.1 分支命名

| 类型 | 格式 | 示例 |
|------|------|------|
| 功能 | `feat/<描述>` | `feat/add-sbom-report` |
| 修复 | `fix/<描述>` | `fix/license-scan-error` |
| 文档 | `docs/<描述>` | `docs/update-contributing-guide` |
| 重构 | `refactor/<描述>` | `refactor/compliance-checker` |

### 3.2 提交信息格式

遵循 [Conventional Commits](https://www.conventionalcommits.org/) 规范：

```
<类型>(<范围>): <简述>

<详细说明>

Signed-off-by: 你的名字 <你的邮箱>
```

**类型列表**：

| 类型 | 说明 |
|------|------|
| `feat` | 新功能 |
| `fix` | Bug 修复 |
| `docs` | 文档变更 |
| `style` | 代码格式（不影响逻辑） |
| `refactor` | 重构 |
| `test` | 测试相关 |
| `chore` | 构建/工具变更 |
| `ci` | CI 配置变更 |

**示例**：

```
feat(compliance): add SPDX SBOM auto-generation

Add automated SBOM generation in SPDX format for all
projects during release builds.

Closes #42

Signed-off-by: Zhang San <zhangsan@example.com>
```

---

## 4. DCO 签署要求

ITrys 采用 **DCO（Developer Certificate of Origin）** 而非 CLA，确保贡献者保留版权。

### 4.1 如何签署

在每次 Git 提交时添加 `Signed-off-by` 行：

```bash
git commit -s
```

这会自动添加：

```
Signed-off-by: 你的名字 <你的邮箱>
```

### 4.2 DCO 含义

通过签署 DCO，你确认：

1. 贡献为本人创作，或有权以声明的许可证提交
2. 贡献以项目声明的开源许可证提供
3. 你理解并同意项目按其许可证使用你的贡献

完整法律文本见：[https://developercertificate.org/](https://developercertificate.org/)

### 4.3 DCO 检查

所有 PR 将自动检查是否包含 `Signed-off-by`，未签署的提交将被阻止合并。

---

## 5. PR 提交规范

### 5.1 PR 模板

```markdown
## 变更说明
简要描述此 PR 的目的和内容

## 关联 Issue
Closes #

## 变更类型
- [ ] 新功能（feat）
- [ ] Bug 修复（fix）
- [ ] 文档变更（docs）
- [ ] 重构（refactor）
- [ ] 其他：___

## 检查清单
- [ ] 代码通过本地测试
- [ ] 已添加必要的测试用例
- [ ] 已更新相关文档
- [ ] 提交信息符合 Conventional Commits 规范
- [ ] 已签署 DCO（git commit -s）
```

### 5.2 PR 审查流程

1. **自动检查**：CI/CD、DCO 验证、许可证扫描
2. **代码审查**：至少 1 名维护者审查
3. **修改迭代**：根据审查意见修改（追加提交，不要 force push）
4. **批准合并**：维护者批准后合并

### 5.3 合并规则

- 使用 **Squash Merge** 保持提交历史整洁
- 合并信息遵循 Conventional Commits 格式
- 合并后自动关闭关联 Issue

---

## 6. 新项目提案（RFC）

如果你想将项目入驻 ITrys，请遵循以下流程：

### 6.1 提案格式

在 `community` 仓库创建 Issue，使用 `project_proposal` 模板，包含：

- 项目名称与简介
- 解决的问题与目标用户
- 技术栈与架构概述
- 开源许可证
- 商业模式声明（如适用）
- 当前状态与路线图
- 维护团队

### 6.2 审核流程

1. 提交提案 → PMC 初审（7 天内）
2. 社区讨论（≥7 天）→ 收集反馈
3. 指导委员会投票 → 通过/拒绝/需修改
4. 通过后进入孵化期

详见 [GOVERNANCE.md](./GOVERNANCE.md#4-项目准入标准)

---

## 7. 社区资源

| 资源 | 链接 |
|------|------|
| 📋 行为准则 | [CODE_OF_CONDUCT.md](./CODE_OF_CONDUCT.md) |
| 🏛️ 治理文档 | [GOVERNANCE.md](./GOVERNANCE.md) |
| 🔒 安全报告 | [SECURITY.md](./SECURITY.md) |
| 💬 社区讨论 | [Discord](https://discord.gg/your-invite-link) |
| 📧 合作咨询 | contact@itrys.org |

---

## 8. 常见问题

### Q: 我是新手，从哪里开始？

寻找标有 `good-first-issue` 的 Issue，这些是适合新贡献者的任务。不要害怕提问，社区会帮助你。

### Q: 我的 PR 多久会被审查？

维护者会尽量在 **7 天内** 首次回复。如果超过 7 天没有回应，可以在 PR 中礼貌地催促。

### Q: 我不同意审查意见怎么办？

友好地说明你的理由。如果无法达成一致，可以请其他维护者参与讨论。

### Q: 我可以贡献商业相关的内容吗？

可以，但须确保不泄露商业机密，且开源部分符合 [商业友好政策](./GOVERNANCE.md)。

---

> **I Try —— 致每一位勇敢迈出开源第一步的你。**
> 你的第一个 PR，我们陪你完成。

---

*最后更新：2026-04-13*
