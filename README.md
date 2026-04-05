# FlyPlugin

一个基于经济系统按时扣费的飞行插件，依赖 Vault 连接服务器经济插件。

## 当前版本

- 插件版本：`1.1.1`
- Paper API：`26.1.1.build.20-alpha`
- Java 要求：`25+`

## 主要功能

- 玩家使用 `/flystart` 开启飞行并开始扣费
- 玩家使用 `/flystop` 关闭飞行并停止扣费
- 支持定时扣费与余额不足自动关闭飞行
- 支持玩家退出、重连时的飞行状态处理
- 支持控制台日志输出与配置热重载

## 运行要求

- Paper 26.1.x
- Java 25+
- Vault
- 任意 Vault 兼容经济插件

## 命令

- `/flystart`
- `/flystop`
- `/flyreload`

## 当前状态

- 当前已完成 26.1 依赖与 Java 25 构建升级
- 已修正 `plugin.yml` 中 Vault 依赖声明
- 已在 Paper 26.1.1 测试服中完成基础功能验证
- 详细升级记录见 [docs/PAPER-26.1-UPGRADE.md](docs/PAPER-26.1-UPGRADE.md)
- 已验证 `/flystart`、`/flystop`、`/flyreload` 以及退出时飞行状态处理

## 构建

```bash
mvn clean package
```

构建完成后可在 `target/` 目录获取插件 jar。

## 许可证

MIT
