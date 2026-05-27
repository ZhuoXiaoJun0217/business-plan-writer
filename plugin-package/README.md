# business-plan-writer

创业计划书自动生成 Claude Code 插件。

## 功能

- 规范文件智能检测与降级（自动适配老师给的规范，无规范时降级为全球标准模板）
- 五步结构化工作流：想法挖掘 → 市场分析 → 方案设计 → 数据搜索 → HTML生成
- 市场分析框架：TAM/SAM/SOM、用户画像、竞争分析、商业模式画布(BMC)、SWOT
- 技术型/服务型项目自动识别，差异化处理
- 真实市场数据搜索与 GB/T 7714 学术引用
- StyleKit 设计风格推荐与学术报告风格 HTML 输出
- 打印友好 CSS（封面、目录、页眉页脚）

## 安装

### 方式一：通过插件市场安装

```bash
# 添加市场
claude /plugin add-marketplace https://github.com/ZhuoXiaoJun0217/business-plan-writer

# 安装插件
claude /plugin install business-plan-writer@business-plan-writer-marketplace
```

### 方式二：手动安装

在 `~/.claude/settings.json` 的 `extraKnownMarketplaces` 中添加：

```json
{
  "extraKnownMarketplaces": {
    "business-plan-writer-marketplace": {
      "source": {
        "source": "url",
        "url": "https://github.com/ZhuoXiaoJun0217/business-plan-writer.git"
      }
    }
  }
}
```

## 使用

```
帮我写一份创业计划书，我的项目是"xxx"。规范文件放在项目文件夹里了。
```

Skill 会自动激活并引导你完成整个流程。

## Benchmark

在 3 个测试用例上 vs 无 skill 基线：

| 指标 | 有 Skill | 无 Skill | 提升 |
|------|---------|---------|------|
| 通过率 | 100% | 63.3% | +36.7% |
| 规范文件检测 | 100% | 33% | +67% |

## 许可证

MIT
