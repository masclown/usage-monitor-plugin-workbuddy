# UsageMonitor Provider Plugin: WorkBuddy

UsageMonitor is a Windows desktop AI usage monitor (.NET 8 / WPF).
This repository hosts the **provider** plugin for **WorkBuddy (CodeBuddy)**, used as a snapshot source by the main project.

> **Decoupled architecture**: This plugin is independently versioned and released. The main project (`masclown/UsageMonitor-src`) declares a pinned version in `plugins.lock.json`. This repo is consumed via `sync-plugin-sources.ps1` during the main project's release.

## Plugin Metadata

| Field | Value |
|---|---|
| Plugin type | `provider` |
| Provider ID | `WorkBuddy` |
| Display name | WorkBuddy |
| Min SDK version | `0.45.0` |
| Credential domains | `workbuddy.cn` |

## Repository Structure

```
.
├── README.md
├── defaults.json   # provider 清单
├── i18n/           # 多语言包
│   ├── zh-CN.json
│   └── en-US.json
├── assets/         # 图标等资源
├── CHANGELOG.md    # 插件独立变更日志
├── LICENSE         # Business Source License 1.1
├── LICENSE-APACHE  # Apache License 2.0
└── .github/workflows/release.yml  # tag v* 触发 → 打 zip → 上传 Release
```

## Versioning & Release

- 此插件**独立版本化**：tag `v<semver>` → 独立 CI 出 zip → 独立 GitHub Release
- 主项目通过 [plugins.lock.json](https://github.com/masclown/UsageMonitor-src/blob/main/plugins.lock.json) 锁定本插件的版本
- 版本号变更流程（主项目目录执行）：

```powershell
.\scripts\bump-plugin.ps1 -Type provider -Id workbuddy -Version <X.Y.Z>
```

## SDK Compatibility Matrix

| UsageMonitor version | Plugin version range | Status |
|---|---|---|
| 0.45.0+ | 1.0.x | tested |
| 0.59.x | 1.0.x | tested |
| latest | latest | tested at release |

## License

Dual-licensed under **Business Source License 1.1** (`LICENSE`) and **Apache License 2.0** (`LICENSE-APACHE`), same as the main project.