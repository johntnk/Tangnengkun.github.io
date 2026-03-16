# 个人介绍网页

这是一个个人介绍网页，包含以下内容：
- 基本资料（头像、姓名、职位）
- 关于我
- 教育经历
- 项目经历
- 联系方式

## 技术栈
- HTML5
- CSS3
- Font Awesome 图标库

## 如何使用

1. 克隆或下载此项目到本地
2. 打开 `index.html` 文件即可查看网页效果
3. 根据需要修改以下内容：
   - 头像：替换 `index.html` 中的头像链接
   - 个人信息：修改 `index.html` 中的姓名、职位、个人描述等
   - 教育经历：修改 `education` 部分的内容
   - 项目经历：修改 `projects` 部分的内容
   - 联系方式：修改 `contact` 部分的内容

## 部署到 GitHub Pages

### 方法一：使用 GitHub 仓库直接部署

1. 在 GitHub 上创建一个新的仓库，命名为 `username.github.io`（其中 `username` 是你的 GitHub 用户名）
2. 将项目文件（index.html、style.css）上传到仓库
3. 进入仓库设置（Settings）
4. 向下滚动到 "GitHub Pages" 部分
5. 在 "Source" 下拉菜单中选择 "main" 分支
6. 点击 "Save" 按钮
7. 等待几分钟，GitHub 会为你生成一个 URL，格式为 `https://username.github.io`

### 方法二：使用 GitHub Actions 部署

1. 在 GitHub 上创建一个仓库
2. 将项目文件上传到仓库
3. 创建 `.github/workflows/deploy.yml` 文件，内容如下：

```yaml
name: Deploy to GitHub Pages

on:
  push:
    branches: [ main ]

jobs:
  deploy:
    runs-on: ubuntu-latest
    steps:
      - uses: actions/checkout@v2
      - name: Deploy to GitHub Pages
        uses: peaceiris/actions-gh-pages@v3
        with:
          github_token: ${{ secrets.GITHUB_TOKEN }}
          publish_dir: .
```

4. 提交并推送更改
5. 进入仓库设置，在 "GitHub Pages" 部分选择 "gh-pages" 分支作为源

## 响应式设计

该网页采用响应式设计，适配不同屏幕尺寸：
- 桌面端：多列布局
- 平板端：适当调整布局
- 移动端：单列布局

## 自定义样式

你可以通过修改 `style.css` 文件来自定义网页样式，例如：
- 更改颜色方案
- 调整字体大小
- 修改布局结构
- 添加动画效果

## 注意事项

- 确保头像图片链接有效
- 替换所有示例内容为你自己的真实信息
- 测试网页在不同设备上的显示效果
- 确保所有链接都能正常工作