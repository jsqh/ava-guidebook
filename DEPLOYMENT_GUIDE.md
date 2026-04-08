# GitHub Pages 部署指南

## 快速开始

本项目已经配置好GitHub Pages所需的全部文件，您只需要按照以下步骤操作即可：

### 1. 推送到GitHub仓库

```bash
# 初始化git仓库（如果还没有）
git init
git add .
git commit -m "Initial commit for GitHub Pages"

# 添加远程仓库（替换为您的仓库地址）
git remote add origin https://github.com/[your-username]/[your-repo-name].git
git push -u origin main
```

### 2. 启用GitHub Pages

1. 在GitHub上打开您的仓库
2. 点击 **Settings** 选项卡
3. 向下滚动到 **Pages** 部分
4. 在 **Source** 部分，选择 **Deploy from a branch**
5. 选择 **main** 分支和 **/ (root)** 目录
6. 点击 **Save**

### 3. 访问您的网站

几分钟后，您的网站将在以下地址可用：
```
https://[your-username].github.io/[your-repo-name]
```

## 本地测试

在推送之前，您可以在本地测试网站：

```bash
# 安装依赖
bundle install

# 本地启动服务器
bundle exec jekyll serve

# 访问 http://localhost:4000
```

## 自定义配置

### 修改网站信息

编辑 `_config.yml` 文件：
```yaml
title: "您的网站标题"
description: "网站描述"
url: "https://[your-username].github.io"
```

### 更换主题

在 `_config.yml` 中修改 `theme` 配置：
```yaml
theme: minima  # 可以改为其他支持的Jekyll主题
```

## 常见问题

### 图片显示问题

确保图片路径正确，使用相对路径：
```markdown
![图片描述](./image.png)
```

### 中文编码问题

所有Markdown文件都已设置为UTF-8编码，确保您的编辑器也使用UTF-8编码。

### 构建失败

1. 检查 `_config.yml` 的YAML语法
2. 确保所有Markdown文件有正确的前置事项
3. 查看GitHub Actions的构建日志获取详细信息

## 获取帮助

如果您遇到问题，请查看：
- [GitHub Pages文档](https://docs.github.com/en/pages)
- [Jekyll文档](https://jekyllrb.com/docs/)