# CONTRIBUTING.md

# 贡献指南

感谢你对 Awesome Happy Horse 1.0 的兴趣！本指南将帮助你完成贡献流程。

## 📋 贡献类型

我们欢迎以下类型的贡献：

### 1. 添加新提示词
- 新的 Happy Horse 1.0 提示词
- 来自 X/Twitter 的优秀案例
- 社区原创内容

### 2. 改进现有内容
- 修正错误的链接
- 改进提示词描述
- 添加更多示例

### 3. 翻译
- 将内容翻译成其他语言
- 改进现有翻译质量

### 4. 文档改进
- 完善使用说明
- 添加教程或技巧
- 改进分类结构

## 🚀 提交流程

### 步骤 1: Fork 仓库
```bash
# 在 GitHub 上点击 Fork 按钮
```

### 步骤 2: 克隆仓库
```bash
git clone https://github.com/YOUR_USERNAME/awesome-happy-horse.git
cd awesome-happy-horse
```

### 步骤 3: 创建分支
```bash
git checkout -b feature/add-your-prompt-name
```

### 步骤 4: 添加内容
在对应的分类文件中添加你的提示词，遵循以下格式：

```markdown
### X.X [提示词标题]

*简短描述（1-2 句话说明这个提示词的特点/用途）。*

**提示词：**
```
[完整的提示词内容]
```

**来源：** [创作者名称](https://x.com/@username) - [帖子链接](https://x.com/...)

**效果说明：**
- 特点 1
- 特点 2
- 适用场景
```

### 步骤 5: 提交更改
```bash
git add .
git commit -m "docs: 添加 [提示词名称] 到 [分类名称]"
git push origin feature/add-your-prompt-name
```

### 步骤 6: 提交 Pull Request
1. 在 GitHub 上进入你的 fork 仓库
2. 点击 "Compare & pull request"
3. 填写 PR 描述
4. 提交

## 📝 内容规范

### 必须包含
- ✅ 完整的提示词文本
- ✅ 原创来源链接（X/Twitter 帖子）
- ✅ 简短描述
- ✅ 正确的分类位置

### 可选包含
- 📹 示例视频链接
- 🖼️ 输入图片（如有）
- 💡 使用技巧

### 禁止内容
- ❌ 侵权内容
- ❌ 虚假来源
- ❌ 重复提交
- ❌ 广告推广

## 🏷️ 分类说明

请根据你的提示词特点选择合适的分类：

| 分类 | 说明 |
|------|------|
| 电影风格 | 电影级拍摄手法、导演风格 |
| 广告与品牌 | 商业广告、产品展示 |
| 社交媒体 | 病毒式传播内容、meme |
| UGC 风格 | 用户生成内容、日常拍摄感 |
| 动漫与动画 | 二次元、动画风格 |
| 短剧与网剧 | 剧情类、连续内容 |
| 视觉特效 | 特效、实验性艺术 |

## 💬 Commit Message 规范

我们遵循 [Conventional Commits](https://www.conventionalcommits.org/) 规范：

- `docs:` 文档更新
- `feat:` 新功能/内容
- `fix:` 修复错误
- `refactor:` 重构
- `style:` 格式调整
- `chore:` 其他维护

示例：
```bash
git commit -m "docs: 添加电影风格提示词示例"
git commit -m "feat: 新增动漫动画分类"
git commit -m "fix: 修正失效的 X 链接"
```

## 🔍 审核流程

1. 维护者会在 48 小时内审核你的 PR
2. 可能需要修改以满足规范
3. 审核通过后合并到主分支
4. 定期发布新版本

## ❓ 需要帮助？

如有任何问题，欢迎：
- 在 Issue 中提问
- 在 Discussions 中讨论
- 联系维护者

---

再次感谢你的贡献！🎉
