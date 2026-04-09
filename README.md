# 🎬 Jaygo 创意空间 · AI 影视创作工作台

<div align="center">

![版本](https://img.shields.io/badge/版本-v28-blue?style=flat-square)
![平台](https://img.shields.io/badge/平台-纯前端单文件-green?style=flat-square)
![API](https://img.shields.io/badge/API-n1n.ai-purple?style=flat-square)
![License](https://img.shields.io/badge/License-Free-orange?style=flat-square)

**一个纯手搓的 AI 影视创作全流程工具，从剧本到分镜图一键生成。**

[快速开始](#-快速开始) · [功能介绍](#-功能介绍) · [即梦代理服务](#-即梦本地代理服务) · [常见问题](#-常见问题)

</div>

---

## ✨ 项目简介

**Jaygo 创意空间** 是一款专为 AI 影视创作设计的全流程工作台，单文件 HTML 无需安装，开箱即用。

覆盖从创意到视频的完整制作链路：
```
📝 剧本创作 → 🎭 分镜提示词 → 🖼️ 资产管理 → 🎨 分镜图生成 → 🎥 视频合成
```

- 🎯 **100+ 版本迭代**，持续优化打磨
- ⚡ **50+ 功能**，覆盖 AI 视频创作全流程
- 🏠 **纯本地运行**，数据存浏览器，无需服务器
- 🌐 **国内直连**，调用 n1n.ai 聚合 API，无需翻墙

---

## 📁 项目结构

```
📦 项目文件
├── Jaygo创意空间正式版v28.html   # 主程序，单文件独立运行
└── dreamina-proxy.zip            # 即梦本地代理服务（可选）
    ├── server.js                 # Express 代理服务器
    ├── package.json              # 依赖配置
    ├── 启动代理.bat               # Windows 一键启动脚本
    └── run.ps1                   # PowerShell 启动脚本
```

---

## 🚀 快速开始

### 第一步：获取 API Key

1. 打开 [n1n.ai 注册页面](https://api.n1n.ai/register?aff=StUA)，使用邮箱注册
2. 登录后进入控制台 → **API Keys** → **Create Key**，生成 `sk-xxx` 格式的密钥
3. 亚洲用户推荐使用香港节点：`https://hk.n1n.ai`

> 💡 **n1n.ai** 是大模型 API 聚合平台，支持 GPT、Gemini、Claude 等，价格优惠，国内直连无需翻墙。

### 第二步：打开工作台

直接用浏览器打开 `Jaygo创意空间正式版v28.html`，无需安装任何依赖。

### 第三步：配置 API

点击右上角 ⚙️ 设置按钮，填入：

| 配置项 | 说明 | 默认值 |
|--------|------|--------|
| API Key | n1n.ai 生成的密钥 | — |
| 接口地址 | API 服务地址 | `https://api.n1n.ai` |
| 文字模型 | 剧本/分镜生成模型 | `gpt-5.4-nano` |
| 图片模型 | 资产/分镜图生成模型 | `gemini-3.1-flash-image-preview` |

填写完成后点击 **🔑 测试连接**，显示 ✅ 即可开始使用。

---

## 🎯 功能介绍

### 📝 Step 1 · 剧本创作

| 功能 | 说明 |
|------|------|
| AI 一键生成剧本 | 输入主题，自动生成完整剧本 |
| 剧本类型 | 支持 📖 故事短片 / 📺 TVC广告 / 🎵 MV |
| 版本优化 | 点击「✨ 优化」生成新版本 |
| 对话修改 | 通过 💬 对话方式精准调整剧本 |
| 文件上传 | 支持 `.txt` / `.md` / `.docx` 格式导入 |

### 🎭 Step 2 · 分镜提示词

- AI 自动拆分剧本为多个镜头，生成 **3 个风格版本**：
  - 🎞️ 写实纪实
  - 🎬 电影叙事
  - 🎨 艺术表现
- 提示词采用时间分段格式（`0-3s`、`3-6s`…），完美适配 **即梦 Seedance 2.0**
- 每个分镜时长可设置 **3~15 秒**
- 内置 10 种分镜模板：起承转合、动作打斗、种草拔草、Vlog纪录、空间穿越、情绪过山车、产品高定、意境留白、双线叙事、超现实

### 🖼️ Step 3 · 资产管理

```
📋 点击「提取资产」→ AI 自动识别剧本中的人物/场景/道具
```

| 资产类型 | 说明 |
|----------|------|
| 👤 人物 | 生成九视图，保持角色形象一致 |
| 🏞️ 场景 | 场景概念图、氛围图 |
| 🎭 道具 | 关键道具特写图 |

- **12 种风格**：3D科幻、写实电影、日系动漫、吉卜力、赛博朋克、水彩等
- **3 种画质**：1K / 2K / 4K
- 支持 **⚡ 批量生成**，一键出图所有资产

### 🎨 Step 4 · 分镜图生成

- 宫格数量：**6 / 9 / 16 / 25** 宫格自由选择
- 画面方向：**横屏 16:9** / **竖屏 9:16**
- 分镜逻辑：
  - 🎯 景别模式（镜头渐进：远→中→近）
  - 📖 剧情模式（情感递进）
  - 🖼️ 分镜模式（自动压缩拆分）
- 支持添加 **📎 资产参考图** 和 **🖼️ 自定义参考图**，保持画面一致性
- 图片下方自动生成**视频提示词（Part 格式）**，一键复制

### 🎥 Step 5 · 视频生成

> 借助即梦官方平台完成最终视频生成：

1. 前往 [即梦官网](https://jimeng.jianying.com)，选择 **Seedance 2.0** 模型
2. 上传分镜图作为参考图，粘贴复制的视频提示词
3. 设置时长和参数，提交生成
4. 生成完毕后用**剪映 / PR** 拼接为完整视频

> 或使用 dreamina-proxy 代理服务（见下文），直接在网页内提交即梦任务。

---

## 🔧 即梦本地代理服务

> `dreamina-proxy` 是一个轻量级 Node.js 代理服务，让网页可以直接调用即梦 CLI 生成视频。

### 前置要求

- **Node.js** >= 14 — [下载安装](https://nodejs.org)
- **dreamina CLI** — 即梦命令行工具

### 安装 dreamina CLI（Windows）

```powershell
$url = "https://lf3-static.bytednsdoc.com/obj/eden-cn/psj_hupthlyk/ljhwZthlaukjlkulzlp/dreamina_cli_beta/dreamina_cli_windows_amd64.exe"
New-Item -ItemType Directory -Force -Path "$HOME\bin"
Invoke-WebRequest -Uri $url -OutFile "$HOME\bin\dreamina.exe"
[Environment]::SetEnvironmentVariable('Path', [Environment]::GetEnvironmentVariable('Path','User') + ';$HOME\bin', 'User')
```

安装后重新打开终端，运行 `dreamina version` 验证安装。

### 启动代理

```bash
# 解压 dreamina-proxy.zip，进入目录后：
npm install --production
node server.js
```

**或者 Windows 双击 `启动代理.bat` 一键启动。**

代理服务启动在 `http://localhost:3456`

### API 接口

| 接口 | 方法 | 说明 |
|------|------|------|
| `/api/status` | GET | 检测 dreamina 状态、登录状态、积分余额 |
| `/api/gen` | POST | 提交视频/图片生成任务 |
| `/api/query?submit_id=xxx` | GET | 查询本地任务状态 |
| `/api/list?gen_status=success&limit=20` | GET | 查看任务列表 |
| `/api/query_result?submit_id=xxx` | GET | 查询 CLI 返回的真实结果 |

### 提交生成任务示例

```json
POST /api/gen

{
  "mode": "text2video",
  "prompt": "一只猫在草地上奔跑，阳光明媚",
  "ratio": "16:9",
  "duration": 5,
  "model": "dreamina_v2"
}
```

支持的 `mode` 值：

| mode | 说明 |
|------|------|
| `text2video` | 文生视频 |
| `image2video` | 图生视频（需传 `images` 数组） |
| `multimodal2video` | 多模态生视频（文本+图片） |
| `text2image` | 文生图 |

### 统一响应格式

```json
{
  "ok": true,
  "data": { ... },
  "error": null
}
```

---

## 🎨 视觉主题

| 主题 | 效果 |
|------|------|
| 🌙 暗黑模式 | 纯黑背景 + 浮动光球 + 毛玻璃卡片 |
| ☀️ 经典模式 | 深蓝黑背景 + 点阵纹理 + 科技网格 |

点击右上角 🌙/☀️ 按钮随时切换。

---

## 💾 数据管理

- 所有数据存储在**浏览器本地**（IndexedDB + localStorage），无需服务器
- 支持**导出项目 JSON** 备份数据，防止数据丢失
- 支持**导入 JSON** 恢复项目

> ⚠️ 建议定期导出备份，清除浏览器缓存会导致数据丢失。

---

## ❓ 常见问题

**Q: 点击生成一直转圈，没有结果？**
> 检查 API Key 和接口地址是否正确，点击设置页的「测试连接」。长剧本生成最多可能需要等待 5 分钟。

**Q: 如何使用主体参考图保持角色一致？**
> 在资产模块上传角色形象图，AI 生成时会参考该形象保持面部特征、服装、风格一致。（仅限 TVC / MV 项目类型）

**Q: 图片生成失败但 API 已扣费？**
> 这是早期版本的响应格式兼容问题，v28 版本已修复。

**Q: 切换项目后看到旧数据？**
> 按 `Ctrl+Shift+R` 强制刷新页面。

**Q: 数据会丢失吗？**
> 数据存在浏览器本地，**定期使用「导出项目」备份**。

**Q: dreamina-proxy 无法连接？**
> 确保已安装 Node.js 和 dreamina CLI，且代理服务正常运行在 `http://localhost:3456`。可通过浏览器访问 `http://localhost:3456` 确认服务状态。

---

## 🙏 支持作者

这是一个**纯手搓的免费工具**，从诞生到现在已历经 100+ 版本迭代。

如果觉得好用，欢迎：
- ⭐ Star 支持一下
- 🐛 提 Issue 反馈问题
- 💝 自愿打赏支持持续迭代

---

<div align="center">

Made with ❤️ by **Jaygo**

</div>
