# 🐍 贪吃蛇游戏 (Snake Game)

一个用原生 HTML5 + CSS + JavaScript 实现的经典贪吃蛇网页游戏。

## 🎮 在线体验

👉 **[点击这里立即游玩](https://zhangjiaran.github.io/snake-game/)**

## 功能特色

- 纯前端实现，无需安装任何依赖，打开即玩
- 键盘（↑ ↓ ← → / W A S D）与触屏滑动双重控制
- 随分数自动提升速度与关卡
- 最高分本地持久化记录（localStorage）
- 支持暂停（P）与重开（R）
- 精致的深色 UI 风格

## 操作说明

| 按键 | 功能 |
|------|------|
| ↑ / W | 向上移动 |
| ↓ / S | 向下移动 |
| ← / A | 向左移动 |
| → / D | 向右移动 |
| P | 暂停 / 继续 |
| R | 重新开始 |
| 触屏滑动 | 移动方向（移动端支持）|

## 计分规则

- 每吃一个食物得 **10 × 当前级别** 分
- 每 100 分升一级，速度同步提升
- 撞墙或撞到自身则游戏结束

## 本地运行

```bash
# 克隆仓库
git clone https://github.com/zhangjiaran/snake-game.git
cd snake-game

# 直接用浏览器打开 index.html 即可
open index.html          # macOS
xdg-open index.html      # Linux
start index.html         # Windows
```

## CI/CD 流水线

项目使用 **GitHub Actions** 实现自动化流水线（见 `.github/workflows/deploy.yml`）：

1. **Validate** — 每次 Push / PR 自动校验 HTML 文件存在性并执行 HTML lint
2. **Deploy** — 主分支（`main`）Push 成功后自动部署到 **GitHub Pages**，几秒内即可在线访问

```
push / PR  →  [Validate HTML]  →  (main only)  →  [Deploy to GitHub Pages]
```

## 技术栈

- HTML5 Canvas
- 原生 CSS3
- 原生 JavaScript（ES6+）
- GitHub Actions + GitHub Pages

## License

MIT
