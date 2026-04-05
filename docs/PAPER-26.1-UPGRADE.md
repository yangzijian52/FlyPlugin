# FlyPlugin Paper 26.1 升级说明

## 概要

本文档记录 `FlyPlugin` 对 Paper 26.1 的兼容升级情况。

- 项目版本：`1.1.1`
- 目标 Paper API：`26.1.1.build.20-alpha`
- 所需 Java 版本：`25+`
- 升级日期：`2026-04-05`

## 本次调整

- `paper-api` 从 `1.21.4-R0.1-SNAPSHOT` 升级到 `26.1.1.build.20-alpha`
- Java 编译目标从 `21` 升级到 `25`
- `plugin.yml` 版本号改为自动读取 Maven 版本
- 修正 `plugin.yml` 中 Vault 依赖键名为 `depend`
- `maven-shade-plugin` 升级到 `3.6.2`

## 说明

- 截至 `2026-04-05`，PaperMC Maven 中 `paper-api` 的 `latest` 与 `release` 仍指向 `26.1.1.build.20-alpha`
- 本插件仍使用 `plugin.yml` 作为入口，本次升级不需要切换到 `paper-plugin.yml`
- 当前优先完成依赖、构建和文档升级，后续仍建议在带 Vault 经济插件的环境中进行服内验证
- 已补充 Maven 资源过滤，确保 `plugin.yml` 中的版本号会正确写入最终产物

## 验证建议

1. 使用 Java 25 运行 `mvn package`。
2. 在装有 `Vault` 与经济插件的 Paper 26.1 服务端测试 `/flystart`、`/flystop`、`/flyreload`。
3. 验证余额不足、离线退出和重新上线后的飞行状态处理是否正常。

## 已完成验证

- 已在 `Paper 26.1.1-20-dev/26.1@d29063d` 环境中完成插件加载测试
- 已验证 `/flystart`、`/flystop`、`/flyreload`
- 已验证玩家退出时会结束飞行流程
