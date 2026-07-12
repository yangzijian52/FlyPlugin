# FlyPlugin

一个基于经济系统按时扣费的飞行插件，依赖 Vault 连接服务器经济插件。

## 当前版本

- 插件版本：`1.1.2`
- Paper API：`26.2.build.56-alpha`
- Java 要求：`25+`

## 主要功能

- 玩家使用 `/flystart` 开启飞行并开始扣费
- 玩家使用 `/flystop` 关闭飞行并停止扣费
- 支持定时扣费与余额不足自动关闭飞行
- 支持玩家退出、重连时的飞行状态处理
- 支持控制台日志输出与配置热重载

## 运行要求

- Paper 26.2
- Java 25+
- Vault
- 任意 Vault 兼容经济插件

## 命令

- `/flystart`
- `/flystop`
- `/flyreload`

## 当前状态

- 当前已完成 Paper 26.2 依赖升级，并继续使用 Java 25 构建
- 已修正 `plugin.yml` 中 Vault 依赖声明
- 详细升级记录见 [docs/PAPER-26.2-UPGRADE.md](docs/PAPER-26.2-UPGRADE.md)
- 本次升级仅更新 Paper API 与发布元数据；插件此前已能在 Paper 26.2 使用，因此未重复进行服内功能测试

## SpigotMC 发布资料

- [SpigotMC 正式资源页](https://www.spigotmc.org/resources/flyplugin.137012/)
- [版本变更记录](CHANGELOG.md)
- [MIT License](LICENSE)

## 构建

```bash
mvn clean package
```

构建完成后可在 `target/` 目录获取插件 jar。

## 许可证

MIT
