# Insite-lab GitHub Organization 部署指南

## 📁 文件结构

```
insite-lab-github/
├── README.md                    # 组织Profile主页（核心）
├── CONTRIBUTING.md              # 贡献指南
├── CODE_OF_CONDUCT.md           # 行为准则
├── assets/
│   ├── banner-dark.svg          # 深色模式Banner
│   └── banner-light.svg         # 浅色模式Banner
├── .github/
│   ├── profile.yml              # 组织配置
│   ├── PULL_REQUEST_TEMPLATE.md # PR模板
│   ├── ISSUE_TEMPLATE/
│   │   ├── bug_report.yml       # Bug报告模板
│   │   └── feature_request.yml  # 功能请求模板
│   └── workflows/
│       ├── snake.yml            # 贡献图Snake动画
│       ├── update-stats.yml     # 自动更新统计
│       └── contributors.yml     # 自动更新贡献者
└── DEPLOY_GUIDE.md              # 本文件
```

## 🚀 部署步骤

### 第一步：创建Profile仓库

GitHub组织的Profile README需要放在一个特殊仓库中：

1. 访问 https://github.com/organizations/Insite-lab/repositories/new
2. 仓库名必须是：`Insite-lab`（与组织名完全相同）
3. 设为 **Public**（必须公开）
4. 勾选 "Add a README file"
5. 点击 Create repository

### 第二步：上传文件

使用Git命令行上传：

```bash
# 克隆仓库
git clone https://github.com/Insite-lab/Insite-lab.git
cd Insite-lab

# 将下载的文件复制到这个目录
cp -r /path/to/insite-lab-github/* .

# 提交并推送
git add .
git commit -m "🎨 Initialize organization profile with interactive experience"
git push origin main
```

或者使用GitHub Web界面直接上传文件。

### 第三步：启用GitHub Actions

1. 进入仓库的 Settings → Actions → General
2. 确保 "Allow all actions" 已选中
3. 进入 Actions 标签页
4. 手动运行 "Generate Snake Animation" 工作流
   - 这会生成 `output` 分支，包含Snake动画SVG

### 第四步：配置组织信息

1. 访问 https://github.com/organizations/Insite-lab/settings/profile
2. 填写组织描述：`Building the future of technology through open source innovation`
3. 填写网站链接：`https://insite-lab.com`
4. 填写联系邮箱：`contact@insite-lab.com`

### 第五步：自定义内容

编辑 `README.md`，替换以下内容：

- [ ] 项目名称（`project-alpha`, `project-beta`）
- [ ] 项目链接
- [ ] 社交媒体链接（Twitter, LinkedIn）
- [ ] 联系邮箱
- [ ] 技术栈图标
- [ ] 组织描述

## 🎨 自定义指南

### 修改Banner

Banner使用SVG格式，可以用文本编辑器或Figma/Illustrator修改。

- `banner-dark.svg` - 深色模式（GitHub Dark主题）
- `banner-light.svg` - 浅色模式（GitHub Light主题）

### 修改配色方案

当前配色：
- 霓虹青：`#00f7ff`
- 霓虹粉：`#ff6b9d`
- 霓虹黄：`#ffd93d`
- 深色背景：`#0d1117`

在SVG文件中搜索替换这些颜色值即可。

### 添加更多项目卡片

复制README中的项目卡片代码块：

```html
<a href="https://github.com/Insite-lab/YOUR-PROJECT">
<picture>
  <source media="(prefers-color-scheme: dark)" srcset="https://github-readme-stats.vercel.app/api/pin/?username=Insite-lab&repo=YOUR-PROJECT&theme=radical&hide_border=true&bg_color=0d1117&title_color=00f7ff&text_color=a8b2d1&icon_color=ff6b9d">
  <source media="(prefers-color-scheme: light)" srcset="https://github-readme-stats.vercel.app/api/pin/?username=Insite-lab&repo=YOUR-PROJECT&theme=default&hide_border=true&title_color=0066cc&text_color=333333">
  <img alt="Project Name" src="..." width="45%">
</picture>
</a>
```

## ⚙️ 工作流说明

### Snake Animation (snake.yml)

- **触发**：每12小时 / 手动 / push到main
- **作用**：生成贡献图Snake动画
- **输出**：`output` 分支的SVG文件

### Update Stats (update-stats.yml)

- **触发**：每天0点 / 手动 / push到main
- **作用**：计算组织统计数据（仓库数、Star数、Fork数）
- **用途**：可在README中展示实时统计

### Contributors (contributors.yml)

- **触发**：每周一 / 手动 / README变更时
- **作用**：自动更新贡献者头像墙
- **注意**：需要在README中添加贡献者标记

## 🔧 故障排除

### Snake动画不显示

1. 确保已手动运行过 `snake.yml` 工作流
2. 检查 `output` 分支是否存在
3. 等待几分钟让GitHub CDN缓存刷新

### 统计图片加载失败

1. 检查仓库是否设为Public
2. GitHub Readme Stats有请求限制，等待几分钟重试
3. 可以替换为自己的Vercel部署

### Banner不显示

1. 确保图片路径正确
2. 检查图片是否在正确位置
3. GitHub有图片大小限制（约1MB）

## 📊 可选增强

### 添加访客计数器

README中已包含，如果需要自定义：

```markdown
<img src="https://visitor-badge.laobi.icu/badge?page_id=Insite-lab.Insite-lab&style=for-the-badge">
```

### 添加GitHub Readme Metrics

在README中添加：

```markdown
![Metrics](https://metrics.lecoq.io/Insite-lab?template=classic&base.header=0&followup=1&languages=1)
```

### 添加实时活动Feed

使用 [github-readme-activity-graph](https://github.com/Ashutosh00710/github-readme-activity-graph)：

```markdown
<img src="https://github-readme-activity-graph.vercel.app/graph?username=Insite-lab&theme=react-dark&hide_border=true&bg_color=0d1117">
```

## 🎯 下一步建议

1. **创建第一个项目仓库** - 让组织看起来活跃
2. **邀请团队成员** - 显示协作文化
3. **编写Blog文章** - 分享技术见解
4. **参与Hacktoberfest** - 吸引开源贡献者

## 📞 支持

如有问题，请：
- 开一个 Issue
- 发送邮件到 contact@insite-lab.com
- 在 Twitter 上 @insitelab

---

**祝你构建出色的开源组织！** 🚀
