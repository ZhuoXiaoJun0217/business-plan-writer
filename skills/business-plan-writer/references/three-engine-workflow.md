# Step 3.3: 三引擎协作 — 四阶段详细流程

> 此文件是 Step 3 技术方案的详细执行手册。当 Step 3.1 判断项目需要技术方案且至少一个引擎可用时，按此流程执行。

---

## 阶段一：技术规划（superpowers 主导，mattpocock 压测）

1. 调用 `superpowers:writing-plans`：撰写技术方案规划，明确目标、范围、排除项
2. 调用 `superpowers:brainstorming`：与技术方案相关的设计决策头脑风暴
3. 调用 `grill-me`（mattpocock）：对技术方案进行压力测试，逐一推敲 design tree 的每个分支，确保方案经得起追问
4. 产出：技术选型矩阵（含决策理由）、系统边界定义、关键风险点

## 阶段二：架构设计（gstack 主导，mattpocock 增强）

1. 调用 gstack `/plan-eng-review`：系统架构评审，锁定数据流、边缘情况、测试策略
2. 调用 gstack `/design-consultation`：产品设计系统构建（如需要 UI）
3. 调用 `grill-with-docs`（mattpocock）：用领域模型挑战设计方案，打磨术语精确性，产出 ADR
4. 调用 `improve-codebase-architecture`（mattpocock）：识别架构深化机会，确保可测试性
5. 产出：架构图（Mermaid）、API 设计概要、数据模型、组件树

## 阶段三：原型实现（mattpocock 主导，superpowers + gstack 配合）

1. 调用 `prototype`（mattpocock）：构建可丢弃原型，快速验证数据模型和状态管理
2. 调用 `tdd`（mattpocock）：以 red-green-refactor 循环做测试驱动开发
3. 调用 `superpowers:test-driven-development`：补齐集成测试，确保测试覆盖率
4. 调用 gstack `/design-html`：生产级 HTML/CSS 实现
5. 产出：可运行的 MVP 原型、测试套件

## 阶段四：评审与验证（三引擎合流）

1. 调用 gstack `/review`：代码审查，检查正确性
2. 调用 `diagnose`（mattpocock）：对审查发现的问题做纪律化诊断（Reproduce → Minimise → Hypothesise → Instrument → Fix）
3. 调用 `superpowers:verification-before-completion`：对照需求逐条验证
4. 如产品可部署，调用 gstack `/qa`：真实浏览器测试
5. 产出：评审报告、问题清单、修复记录

---

## 引擎不可用时的简化

- 某个引擎不可用 → 跳过该引擎负责的步骤，用剩余引擎完成
- 仅一个引擎可用 → 只执行该引擎的步骤，其余用内置最佳实践
- 全部不可用 → 使用 SKILL.md 3.5 节的全内置后备流程

核心原则：有哪个用哪个，不等待。永远不因依赖缺失而中断工作流。
