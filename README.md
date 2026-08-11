[README.md](https://github.com/user-attachments/files/30932439/README.md)
# 东方角色提示词生成器

一个无需安装、无需服务器、可以直接在浏览器中运行的中文角色提示词生成器，尤其适合东方仙侠、武侠、修仙及架空幻想角色设计。

<img width="1440" height="960" alt="preview" src="https://github.com/user-attachments/assets/4a9bf1c6-03a0-4eee-a408-2df3d67f991d" />


## 功能特点

- 五个完整设计模块：脸型/面部、发型、服装、配饰、武器
- 97 个可组合字段，覆盖面部骨相、眉眼、鼻唇、肤质、服装材质及武器结构等细节
- 同时支持下拉选择、多选、自定义补充及按字段启用
- 实时生成自然组织的中文提示词，不是简单的“字段：值”罗列
- 生成顺序固定为：角色基础信息 → 面部 → 发型 → 服装 → 配饰 → 武器 → 材质细节 → 一致性约束
- 内置角色一致性锁定，适合连续出图、三视图和 AI 视频
- 提供可编辑的负面约束
- 支持随机生成角色、一键复制、清空全部
- 支持浏览器本地保存、读取，以及 JSON 配置导入和导出
- 桌面端优先，并兼容手机和平板
- 完全离线运行，不使用外部依赖，不上传用户数据

## 在线使用

仓库开启 GitHub Pages 后，可直接通过 Pages 提供的网址访问。部署步骤见下方“发布到 GitHub Pages”。

## 本地使用

下载本仓库，然后双击 `index.html` 即可。

也可以点击 GitHub 仓库页面右上方的 `Code` → `Download ZIP`，解压后打开 `index.html`。

## 使用方法

1. 在顶部填写角色名称、性别、年龄段、角色类型和核心气质。
2. 从左侧依次进入脸型/面部、发型、服装、配饰和武器模块。
3. 勾选需要写入提示词的字段，并选择合适的选项。
4. 如果现有选项不合适，在对应项目的“自定义补充”中输入内容。
5. 在右侧检查实时生成的完整角色提示词。
6. 根据需要编辑“一致性锁定”和“负面约束”。
7. 点击“复制完整提示词”，用于 AI 图片或视频生成工具。

## 发布到 GitHub Pages

1. 在 GitHub 创建一个公开仓库，例如 `oriental-character-prompt-generator`。
2. 将本目录中的全部文件上传到仓库根目录。
3. 打开仓库的 `Settings` → `Pages`。
4. 在 `Build and deployment` 中选择 `Deploy from a branch`。
5. Branch 选择 `main`，目录选择 `/ (root)`，然后保存。
6. 等待部署完成，GitHub 会在 Pages 设置页面显示访问地址。

通常访问地址会是：

```text
https://你的用户名.github.io/oriental-character-prompt-generator/
```

## 项目结构

```text
oriental-character-prompt-generator/
├── index.html          # 完整应用，CSS 和 JavaScript 均已内嵌
├── README.md           # 项目说明
├── LICENSE             # MIT 开源许可证
├── CONTRIBUTING.md     # 参与贡献指南
├── .gitignore          # Git 忽略规则
├── .nojekyll           # 禁用不必要的 Jekyll 处理
└── assets/
    └── preview.png     # 项目界面预览
```

## 数据与隐私

本项目不包含服务器端代码，也不会向网络发送角色配置。

“保存配置”使用浏览器的 `localStorage`。清除浏览器站点数据后，本地保存的配置可能会消失；重要配置建议同时使用“导出 JSON”备份。

## 浏览器兼容性

推荐使用较新的 Chrome、Edge、Firefox 或 Safari 浏览器。复制功能会优先使用浏览器剪贴板接口，并提供兼容性回退。

## 开发

项目是一个无构建步骤的单文件静态应用。修改 `index.html` 后刷新浏览器即可查看结果，不需要安装 Node.js 或其他依赖。

欢迎通过 Issue 提交建议、补充角色选项，或通过 Pull Request 改进界面与提示词组织方式。

## 开源许可

本项目使用 [MIT License](LICENSE)。你可以自由使用、修改和分发本项目，但需要保留原许可证与版权声明。

