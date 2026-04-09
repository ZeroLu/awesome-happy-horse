# Awesome Happy Horse 1.0

[![Awesome](https://awesome.re/badge.svg)](https://github.com/sindresorhus/awesome)
[![License: CC BY 4.0](https://img.shields.io/badge/License-CC_BY_4.0-lightgrey.svg)](https://creativecommons.org/licenses/by/4.0/)

> 精选的 Happy Horse 1.0 提示词、视频生成技术和资源合集，助你充分发挥 AI 视频模型的潜力。

<div align="center">

| [English](README.md) | [简体中文](README-zh.md) |
|----------------------|--------------------------|

</div>

---

**最后更新：** 2026 年 4 月

Happy Horse 1.0 是一个**150 亿参数统一 Transformer 模型**，可从文本或图像提示生成视频和同步音频，支持电影级 1080p 画质和 7 种语言的唇形同步。完全开源，支持商业用途。

## 🐴 为什么选择 Happy Horse 1.0？

| 特性 | Happy Horse 1.0 | Seedance 2.0 | LTX-2.3 |
|------|-----------------|--------------|---------|
| 模型规模 | 15B (统一架构) | ~4.5B | 22B |
| 架构类型 | 单流 Transformer | 扩散 Transformer | 双流架构 |
| 文生视频 Elo | **1355** | 1273 | 1290 |
| 图生视频 Elo | **1404** | 1357 | 1345 |
| 去噪步数 | **8 步** (DMD-2) | 25-50 步 | 12-20 步 |
| 1080p 渲染时间 | **~38 秒** (H100) | ~55 秒 | ~45 秒 |
| 唇形同步语言 | **7 种语言** (原生) | 需外部工具 | 有限支持 |
| 开源 | ✅ **是** | ❌ 否 | ✅ 是 |

**胜率：** 80.0% vs OVI 1.1 · 60.9% vs LTX 2.3

---

## 📑 目录

- [电影风格](#1-电影风格)
- [广告与品牌](#2-广告与品牌)
- [社交媒体与病毒内容](#3-社交媒体与病毒内容)
- [UGC 风格](#4-ugc 风格)
- [动漫与动画](#5-动漫与动画)
- [短剧与网剧](#6-短剧与网剧)
- [视觉特效与实验风格](#7-视觉特效与实验风格)
- [资源链接](#8-资源链接)
- [贡献指南](#9-贡献指南)

---

## 🎬 核心能力

Happy Horse 1.0 的统一多模态架构专为联合视频和音频生成而设计：

- **🎯 统一 Transformer：** 40 层自注意力网络，含模态特定层
- **🎵 联合视频 + 音频：** 单次通过生成同步对话、环境音和音效
- **⚡ 8 步 DMD-2 蒸馏：** 无需分类器自由引导的快速生成
- **🌍 多语言唇形同步：** 英语、普通话、粤语、日语、韩语、德语、法语
- **📺 1080p 输出：** 5-8 秒电影级画质片段
- **🔓 开源可自托管：** 完整权重，支持商业用途

---

## 📑 目录

- [资源链接](#资源链接)
- [安装与部署](#安装与部署)
- [提示词工程指南](#提示词工程指南)
- [贡献指南](#贡献指南)

---

## 资源链接

### 官方资源

- [🏠 Happy Horse 官网](https://happyhorses.io) - 官方网站，含演示和文档
- [📦 GitHub 仓库](https://github.com/happy-horse/happyhorse-1) - 源代码和模型权重
- [📄 技术报告](https://happyhorses.io/report) - 完整架构和基准测试详情
- [🎮 在线演示](https://happyhorse.app) - 免费试用 Happy Horse 1.0

### 社区与资讯

- [🔥 Brent Lynch - 来源揭秘](https://x.com/BrentLynch/status/2041903421851365838) - Happy Horse 来自阿里通义实验室（前 Kling 团队负责人）
- [📊 GMI Cloud - 对比测试](https://x.com/gmi_cloud/status/2041952066873221288) - Happy Horse vs Veo, Kling, SkyReel, PixVerse
- [⚠️ 虚假内容警告](https://x.com/BrentLynch/status/2041997193373237561) - 警惕 Seedance 2.0 冒充 Happy Horse
- [FaceSwap-AI 宣布](https://x.com/chennnhhe/status/2041914942509740035) - "开源 AI 视频的 Sora 时刻"
- [HappyhorseAI 官方](https://x.com/Happyhorseteam/status/2041909880496517550) - 官方发布公告
- [Textideo 深度分析](https://textideo.com/blog/happy-horse-1-0-redefining-open-source-sota-ai-video-generation) - 技术深度解析
- [AI Research 周报](https://x.com/airesearch_ai/status/2041638371538432256) - 每周 AI 新闻精选

### 对比与基准测试

- [Artificial Analysis Video Arena](https://artificialanalysis.ai) - Happy Horse 排名第一的排行榜
- [模型对比表](https://happyhorses.io#compare) - 与 Seedance 2.0、LTX-2.3、OVI 1.1 的对比

---

## 安装与部署

### 系统要求

- **GPU：** NVIDIA H100 或 A100（推荐 ≥48GB 显存）
- **存储：** 约 30GB 用于模型权重
- **内存：** 推荐 64GB RAM

### 快速开始

```bash
# 克隆仓库
git clone https://github.com/happy-horse/happyhorse-1.git
cd happyhorse-1

# 安装依赖
pip install -r requirements.txt

# 下载模型权重
bash download_weights.sh

# 生成你的第一个视频
python demo_generate.py --prompt "a robot dancing on the moon" --duration 5
```

### Python API

```python
from happyhorse import HappyHorseModel

model = HappyHorseModel.from_pretrained("happy-horse/happyhorse-1.0")

video, audio = model.generate(
    prompt="一位老人站在山峰上俯瞰山谷",
    duration_seconds=5,
    fps=24,
    language="zh",
)

video.save("output.mp4")
audio.save("output.wav")
```

### 性能基准

| 分辨率 | 时间 (H100) | 适用场景 |
|--------|-------------|----------|
| 256p 预览 | ~2.0 秒 | 快速迭代 |
| 540p + 超分 | ~8.0 秒 | 社交媒体 |
| 1080p 高清 | ~38.4 秒 | 生产质量 |

---

## 提示词工程指南

### 最佳实践

1. **具体描述：** 包含光线、摄像机角度和动作的详细信息
2. **音频提示：** 提及对话、环境音或音乐风格
3. **语言选择：** 为对话场景指定唇形同步语言
4. **时长控制：** 提示词与 5-8 秒输出长度对齐

### 示例提示词结构

```
[风格/类型]：电影级，戏剧性灯光
[主体]：主要角色描述和动作
[场景]：环境和背景细节
[摄像机]：镜头类型、移动、角度
[音频]：对话语言、环境音、音乐风格
[时长]：5-8 秒
```

### 社区示例提示词

来自 @BrentLynch 的 X 收藏夹：

```
手电筒光束探索洞穴系统，照亮湿润的石灰岩地层。
光线捕捉到结晶的方解石沉积物，闪烁着光芒。
光束穿过浅水区时，在水底形成明亮的焦散图案。
钟乳石随着手电筒移动投下长长的、摆动的阴影。

音频：滴水声在洞穴中回响，脚步声踩在湿岩石上，封闭空间中的呼吸声。
```

**为什么这个提示词有效：**
- ✅ 详细的环境描述（洞穴系统、湿石灰岩）
- ✅ 动态光影效果（手电筒光束、晶体闪烁、阴影）
- ✅ 水面效果（浅水、焦散图案）
- ✅ 运动元素（光束移动、阴影摆动）
- ✅ 音频提示（滴水声、脚步声、呼吸声）
- ✅ 空间感（封闭空间声学）

### 多语言支持

Happy Horse 1.0 原生支持 7 种语言的唇形同步：
- 🇺🇸 英语
- 🇨🇳 普通话（含方言）
- 🇭🇰 粤语
- 🇯🇵 日语
- 🇰🇷 韩语
- 🇩🇪 德语
- 🇫🇷 法语

---

## 贡献指南

欢迎贡献！如果你有优秀的 Happy Horse 1.0 提示词或资源，请提交 Pull Request。

### 如何贡献

1. Fork 本仓库
2. 创建新分支 (`git checkout -b feature/add-new-prompt`)
3. 在相应部分添加你的提示词/资源
4. 提交 PR

**请确保包含以下内容：**
- 完整提示词文本（如适用）
- 来源链接（原创者的 X/Twitter 帖子）
- 风格/效果简述
- 示例视频或图片（如有）

### 贡献模板

```markdown
### [你的标题]

*简述。*

**提示词：**
```
[你的提示词]
```

**来源：** [创作者名称](https://x.com/@username) - [帖子链接](https://x.com/...)

**设置：**
- 时长：5 秒
- 语言：中文
- 分辨率：1080p
```

---

## 许可证

[![CC BY 4.0](https://img.shields.io/badge/License-CC_BY_4.0-lightgrey.svg)](https://creativecommons.org/licenses/by/4.0/)

本作品采用 [知识共享署名 4.0 国际许可协议](https://creativecommons.org/licenses/by/4.0/) 进行许可。

Happy Horse 1.0 模型权重在允许商业用途的许可下发布。

---

<div align="center">

**觉得有帮助？** ⭐ Star 支持社区！

🐴 由 Happy Horse 社区 ❤️ 构建

</div>
