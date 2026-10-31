# 日日 · 每日计划与目标

一个移动端友好的「每日计划 + 目标打卡」网页应用。单文件即可运行，可直接部署到 GitHub Pages 在线使用。

## 功能

- **今日**：今天与明天的详细计划、未来 7 天概览；进度环 + 步骤条 + 数字滚动。
- **计划**：未来 21 天日期选择，支持拖拽排序、点击修改、卡片删除、标签。
- **目标**：独立设置目标（标记目标时间），目标日前每日打卡，进度与倒计时。
- **交互**：主题切换（圆形扩散切深色）、勾选动效、标签放大让位、删除飞行动画、打卡盖章等。
- **数据**：保存在浏览器本地（localStorage），无需账号即可使用。

## 本地使用

直接双击 `index.html` 用浏览器打开即可，建议 Chrome / Safari / Edge 等现代浏览器。

## 上线到 GitHub Pages

1. 注册并登录 [GitHub](https://github.com)。
2. 右上角 `+` → `New repository`，仓库名填 `daily-planner`，选 **Public**，不要勾选「Add a README file」，点 `Create repository`。
3. 进入仓库页，点 `Add file` → `Upload files`，把本文件夹里的 `index.html` 和 `README.md` 拖进去，点 `Commit changes`。
4. 打开仓库的 `Settings` → 左侧 `Pages`，在 **Branch** 处选 `main` 和 `/(root)`，点 `Save`。
5. 等 1～2 分钟，访问 `https://你的用户名.github.io/daily-planner/` 即可在线使用。

也可以用命令行上传：

```bash
cd daily-planner
git init
git add index.html README.md
git commit -m "init"
git branch -M main
git remote add origin https://github.com/你的用户名/daily-planner.git
git push -u origin main
```

## 数据说明

当前数据存在浏览器本地 localStorage，换设备或清除浏览器数据会丢失。如需多端同步，可后续接入后端（如 Supabase、云函数），替换 `Store` 存储层即可，界面无需改动。

## 目录

- `index.html` — 应用本体（单文件，含 HTML / CSS / JS）
- `README.md` — 本说明
