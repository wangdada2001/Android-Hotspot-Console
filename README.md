# Android-Hotspot-Console

Android Hotspot Console 0.5.5（lite / obfuscated）构建产物，已改为从本仓库检查更新。

## 下载

| 文件 | 大小 | 说明 |
| --- | --- | --- |
| `Android_Hotspot_Console_0.5.5_lite_obfuscated.zip` | 9.63 MB | v0.5.5 lite 混淆版，内置本仓库更新通道 |

直接下载：

```
https://github.com/wangdada2001/Android-Hotspot-Console/raw/main/Android_Hotspot_Console_0.5.5_lite_obfuscated.zip
```

## 更新检查

模块使用 Magisk 标准的 `updateJson` 机制：

- 包内 `module.prop`：`updateJson=https://raw.githubusercontent.com/wangdada2001/Android-Hotspot-Console/main/update.json`
- 仓库根目录 `update.json` 提供 `version` / `versionCode` / `zipUrl` / `changelog`

发布新版本时，只需：

1. 上传新的 zip 并命名（或覆盖同名文件）；
2. 修改 `update.json` 里的 `version`、`versionCode`，确保 `zipUrl` 指向新包；
3. Magisk / Kitsune 的模块页就会出现更新按钮，并从本仓库下载。
