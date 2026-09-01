# UsageMonitor Provider Plugin: WorkBuddy

WorkBuddy (CodeBuddy) provider plugin for the UsageMonitor ecosystem.

> Independent plugin repository. Independently versioned and released.

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
└── LICENSE-APACHE  # Apache License 2.0
```

## Versioning & Release

- 独立版本化：tag `v<semver>` → 独立 zip → 独立 Release
- 版本号变更流程：在主项目目录运行

  ```powershell
  .\scripts\bump-plugin.ps1 -Type provider -Id workbuddy -Version <X.Y.Z>
  ```

## License

Licensed under **Apache License 2.0** (`LICENSE-APACHE`), consistent with the main project's SDK / declaration pack licensing model.