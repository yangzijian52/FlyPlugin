# FlyPlugin Paper 26.2 升级说明

## 概要

本文档记录 `FlyPlugin` 对 Paper 26.2 的版本升级情况。

- 项目版本：`1.1.2`
- 目标 Paper API：`26.2.build.56-alpha`
- 所需 Java 版本：`25+`
- 升级日期：`2026-07-11`

## 本次调整

- `paper-api` 从 `26.1.1.build.20-alpha` 升级到 `26.2.build.56-alpha`
- `plugin.yml` 中的 `api-version` 更新为 `26.2`
- 项目版本从 `1.1.1` 更新为 `1.1.2`
- README 中的版本、运行要求和升级记录同步更新

## 验证

- 使用 Java 25 完成 Maven 编译与打包
- 核对最终 jar 内的 `plugin.yml`，确认插件版本、API 版本与 Vault 依赖声明正确
- 该插件升级前已能在 Paper 26.2 正常使用，本次未重复进行服内功能测试
