# Changelog

## usage-monitor-plugin-workbuddy 1.2.0 (2026-09-05)

- 移除 meta.iconUrl / meta.iconUrlDark，logo 改为运行时从网页 favicon 抓取（宿主按主题选择可渲染资源）。

## usage-monitor-plugin-workbuddy 1.1.0 (2026-09-05)

- 对齐主仓 `src/Plugins/UsageMonitor.Plugin.WorkBuddy` 权威 defaults.json 与 i18n 词条。
- `used_credits` 语义统一为全局总消耗（`TotalDosage`）；per-account 用量改经 `quota_rows.used` 保留（Stage-5 字段规范化）。
- 额度行 `quota_type` 改 `literalValue: "purchase"`，移除 `get-user-resource-summary` 聚合段与旧的 subscription/gift valueMap。
- 迷你圆环补齐平台奖励积分，统一展示套餐积分与奖励积分的总额/已用/剩余。

## workbuddy 1.0.0 (2026-09-01)

Initial release as an independent plugin repository.

Migrated from `src/Plugins/UsageMonitor.Plugin.WorkBuddy/` in the main project.
The contents of this repo at this tag match the v1.0.0 snapshot from the main project before the plugin-repository-split refactor.
