# DataEase Plugins

DataEase 插件仓库，汇总数据源插件、数据填报插件与视图插件示例，用于扩展 DataEase 的连接能力、填报能力和可视化能力。

## 📖 项目简介

本仓库用于维护和展示 DataEase 插件工程示例。开发者可以基于现有插件结构，快速创建新的扩展模块，并通过标准化目录、元数据和构建方式集成到 DataEase 中。

当前仓库主要包含三类插件：

- **数据源插件**：扩展新的数据库、数仓或查询引擎接入能力
- **数据填报插件**：扩展不同数据库的数据填报能力
- **视图插件**：扩展图表、表格和其他可视化组件能力

## 🚀 现有插件

### 数据源插件

- **Apache Hive 数据源插件** - 提供 Hive 数据源接入能力

### 数据填报插件

- **PostgreSQL 数据填报插件** - 提供 PostgreSQL 数据填报能力

### 视图插件

- **ECharts 组合图插件** - 提供组合图可视化能力

## 📁 项目结构

```text
extensions/
├── README.md             # 仓库说明文档
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
└── view-xxx/             # 视图插件，命名规范为 view-*
│   │   ├── data.yaml     # 配置
│   │   ├── logo.png      # 图标
│   │   ├── README.md     # 说明
│   │   └── 1.0.0/        # 版本目录
```

## 🛠️ 注意事项
1. 必须包含 data.yaml、logo.png、README.md 以及至少一个版本目录（如 1.0.0）。如果有多个版本，则需创建相应数量的版本目录，例如 1.0.0、1.0.1 等。
2. README.md 文件应详细描述插件信息，包括但不限于插件介绍、功能、使用说明、参数说明及调用示例。其中引用的所有图片或 GIF 需托管于公网地址上（例如 OSS 或网盘）以便正确显示。
3. 对于插件类模板，务必在 README.md 中明确记录输入输出参数及其调用方法；对于智能体类，若存在父子嵌套结构，需在 README.md 中清晰描述其调用关系，并确保被调用的子智能体文件也存储于公网地址（如 OSS 或网盘）。
4. 在 data.yaml 文件中：
   - name: 插件名称，例如“合同审核智能体”。
   - tags: 与 tools 下的 data.yaml 中保持一致，例如 ["数据源插件"]。可参考https://apps.fit2cloud.com/dataease 分类标签，切勿写错字。
   - title: 在插件商店展示的简短描述，例如“用于审核合同内容并提供智能建议的应用。”
   - edition: 插件适用的 DataEase 版本类型，例如 community 或 enterprise，需与插件实际支持的发行版保持一致
   - description: 导入到 DataEase 的详细描述，可以与 title 相同。
```yaml
name: TDEngine 数据源插件
tags:
  - 数据源插件    # 或 数据填报插件、视图插件等
title: TDEngine 数据源插件
edition: enterprise
description: 基于 TDEngine 3.3.6.13 开发，要求 DataEase 版本 >= 2.10.21  
```

## 🤝 贡献指南

如果您想为 DataEase Toolstore 贡献新的插件，请参考：
[如何提交自己想要的插件](./如何提交插件.md)

### 插件开发规范

- 每个插件需要包含 `data.yaml` 配置文件
- 提供清晰的插件说明文档
- 包含适当的图标和版本管理
- 遵循 DataEase 平台的开发规范


## 📞 联系我们

- 项目地址：https://github.com/dataease/dataease-plugins
- 问题反馈：请在 GitHub Issues 中提交
- 文档支持：参考 DataEase 官方文档