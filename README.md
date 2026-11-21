# Android-Hotspot-Console

Android Hotspot Console 0.5.5（lite / obfuscated）构建产物，模块更新走本仓库的 Releases。

## 下载

| 版本 | 文件 | 大小 | 适用 |
| --- | --- | --- | --- |
| 0.5.5 | `Android_Hotspot_Console_0.5.5_lite_obfuscated.zip` | 9.63 MB | arm64、Android 10+、已 Root |

在 Releases 页下载：

https://github.com/wangdada2001/Android-Hotspot-Console/releases/latest

## 安装

1. 用 Magisk / Kitsune 选择本 zip 覆盖安装（不支持 recovery 刷入）；
2. 安装完成后重启手机，解锁屏幕（部分功能需要解锁后才会启动）；
3. 手机浏览器打开 http://127.0.0.1:8080 ，密码状态保存在 `/data/adb/oneplus-hotspot`。

初始密码（如首次安装）可用以下命令读取：

```
su -c 'cat /data/adb/oneplus-hotspot/initial-password.txt'
```

升级不会清空原有登录设置、流量历史和转发规则。

## 更新检查

模块使用 Magisk 标准的 `updateJson` 机制：

- 包内 `module.prop`：`updateJson=https://raw.githubusercontent.com/wangdada2001/Android-Hotspot-Console/main/update.json`
- 仓库 `update.json` 提供 `version` / `versionCode` / `zipUrl`（指向 Releases 资产）/ `changelog`

发布新版本时：

1. 新建 Releases，带上新 zip 资产；
2. 修改 `update.json` 里的 `version`、`versionCode` 和 `zipUrl`；
3. Magisk / Kitsune 模块页会出现更新按钮，并从 Releases 下载。
