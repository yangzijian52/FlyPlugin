# FlyPlugin 🚀

> 适用于 Minecraft 服务器的经济飞行插件 

![Version](https://img.shields.io/badge/Version-1.1.0-blue)
![Paper](https://img.shields.io/badge/Paper-1.21.4-red)
![Java](https://img.shields.io/badge/Java-21-orange)

## 📖 简介
基于经济系统的飞行管理插件，实现以下核心功能：
- 按分钟计费的飞行模式
- 退出游戏自动停止计费
- 高度可配置的经济参数
- 实时日志监控

## ✨ 功能列表
- ✅ `/flystart` - 开启飞行并开始计费
- ✅ `/flystop` - 立即停止飞行和计费
- ✅ 离线自动保存飞行状态
- ✅ 玩家退出自动停止计费
- ✅ 支持所有 Vault 兼容的经济插件
- ✅ 实时控制台日志记录

## ⚙️ 技术规格
| 类别        | 要求                          |
|------------|------------------------------|
| 服务端核心   | Paper 1.21.4 或兼容分支       |
| Java 版本   | JDK 21                       |
| 前置插件     | Vault, XConomy (或其它经济插件)|

## 📦 安装指南

### 1. 下载插件
从 [Releases](https://github.com/yourname/FlyPlugin/releases) 页面下载最新版本

### 2. 安装到服务器

将插件放入 plugins 文件夹

### 3. 安装到服务器

Vault (必选)

XConomy 或其它经济插件

## ⚡ 快速开始
启动/重启服务器

玩家输入指令：

/flystart  # 开启飞行（立即扣除首分钟费用）

/flystop   # 关闭飞行

## 🔧 配置文件 (config.yml)
### 经济设置(默认)
settings:
  cost-per-minute: 0.1    # 每分钟费用
  
  charge-interval: 60     # 扣费间隔（秒）
  
  console-logging: true    # 启用日志

## 📜 命令列表

| 命令        | 权限节点             |描述  |
|------------|----------------------|-----------------------|
| /flystart   | flyplugin.use       |  开启飞行并开始计费  |
| /flystop   | flyplugin.use        | 停止飞行和计费  |
| /flyreload     |flyplugin.admin   |重载配置文件|




## 💡 常见问题
Q: 为什么无法扣费？
A: 确保已安装 Vault 和经济插件，并在控制台输入 /vault 验证经济系统连接状态

Q: 如何修改扣费周期？
A: 编辑 config.yml 中的 charge-interval 值（单位：秒）后执行 /flyreload


