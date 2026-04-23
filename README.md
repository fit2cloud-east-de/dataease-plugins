# DataEase Plugins

DataEase 插件仓库，汇总数据源插件、数据填报插件与图表插件示例，用于扩展 DataEase 的连接能力、填报能力和可视化能力。

## 📖 项目简介

本仓库用于维护和展示 DataEase 插件工程示例。开发者可以基于现有插件结构，快速创建新的扩展模块，并通过标准化目录、元数据和构建方式集成到 DataEase 中。

当前仓库主要包含三类插件：

- **数据源插件**：扩展新的数据库、数仓或查询引擎接入能力
- **数据填报插件**：扩展不同数据库的数据填报能力
- **图表插件**：扩展图表、表格和其他可视化组件能力

## 🚀 现有插件

### 数据源插件

- **Apache Hive 数据源插件** - 提供 Hive 数据源接入能力

### 数据填报插件

- **PostgreSQL 数据填报插件** - 提供 PostgreSQL 数据填报能力

### 图表插件

- **ECharts 组合图插件** - 提供组合图可视化能力

## 📁 项目结构

```text
extensions/
├── ds-xxx/               # 数据源插件，命名规范为 ds-*
│   │   ├── data.yaml     # 配置
│   │   ├── logo.png      # 图标
│   │   ├── README.md     # 说明
│   │   └── 1.0.0/        # 版本目录
├── df-xxx/               # 数据填报插件，命名规范为 df-*
│   │   ├── data.yaml     # 配置
│   │   ├── logo.png      # 图标
│   │   ├── README.md     # 说明
│   │   └── 1.0.0/        # 版本目录
└── view-xxx/             # 图表插件，命名规范为 view-*
│   │   ├── data.yaml     # 配置
│   │   ├── logo.png      # 图标
│   │   ├── README.md     # 说明
│   │   └── 1.0.0/        # 版本目录
```

## 🛠️ 注意事项
1. 必须包含 data.yaml、logo.png、README.md 以及至少一个版本目录（如 1.0.0）。如果有多个版本，则需创建相应数量的版本目录，例如 1.0.0、1.0.1 等。
2. README.md 文件应详细描述插件信息，包括但不限于插件介绍、功能、使用说明、参数说明及调用示例。
3. 在 data.yaml 文件中：
   - name: 插件名称，例如“Oracle 数据填报插件”。
   - title: 在插件商店展示的简短描述。
   - description: 导入到 DataEase 的详细描述，可以与 title 相同。
   - tags: 与 extensions 下的 data.yaml 中保持一致，例如 ["数据源插件"]。可参考https://apps.fit2cloud.com/dataease 分类标签，切勿写错字。
   - additionalProperties: 扩展字段
     - dataease_version: 是否为企业版功能
```yaml
name: Oracle 数据填报插件
title: Oracle 数据填报插件
description: 基于 Oracle 21c 开发，推荐使用 DataEase v2.10.21 版本
tags:
  - 数据填报插件
additionalProperties:
  enterprise: true
```

## 🤝 贡献指南

如果您想为 DataEase Toolstore 贡献新的插件，请参考：
[如何提交自己想要的插件](./如何提交自己的插件.md)

### 插件开发规范

- 每个插件需要包含 `data.yaml` 配置文件
- 提供清晰的插件说明文档
- 包含适当的图标和版本管理
- 遵循 DataEase 平台的开发规范


## 📞 联系我们

- 项目地址：https://github.com/dataease/dataease-plugins
- 问题反馈：请在 GitHub Issues 中提交
- 文档支持：参考 DataEase 官方文档