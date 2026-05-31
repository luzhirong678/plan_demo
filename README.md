# 🎮 霓虹贪吃蛇

一个采用霓虹街机风格的网页版贪吃蛇游戏，功能完整、用户体验优秀。

## ✨ 功能特性

- 🐍 经典贪吃蛇玩法
- 🎨 霓虹发光视觉效果
- ⌨️ 键盘控制（方向键/WASD）
- 📱 触摸滑动控制
- 📊 分数和等级系统
- 💾 本地存储最高分
- 📱 响应式设计
- ⚡ 流畅的动画（60fps）

## 🚀 快速开始

### 运行游戏

直接在浏览器中打开 `index.html` 文件即可。

### 操作说明

| 操作 | 按键 |
|------|------|
| 上移 | ↑ / W |
| 下移 | ↓ / S |
| 左移 | ← / A |
| 右移 | → / D |
| 暂停/继续 | 空格键 / P |

移动端可以在屏幕上滑动方向。

## 📁 项目结构

```
plan_demo/
├── index.html              # 游戏主文件
├── README.md               # 项目说明
├── CHANGELOG.md            # 变更日志
├── COMMIT_CONVENTION.md    # Commit 规范
├── 测试报告.md             # 测试报告
└── .trae/
    └── documents/
        ├── PRD.md          # 产品需求文档
        └── 技术架构文档.md # 技术架构文档
```

## 🏗️ 技术架构

- **渲染技术**: HTML5 Canvas 2D
- **编程语言**: 原生 JavaScript (ES6+)
- **样式**: CSS3 (Flexbox, Grid, 动画)
- **字体**: Google Fonts (Press Start 2P, Orbitron, Roboto)

### 核心类

| 类名 | 功能 |
|------|------|
| `GameController` | 游戏主控制器 |
| `Snake` | 蛇身管理 |
| `Food` | 食物生成 |
| `CollisionDetector` | 碰撞检测 |
| `ScoreManager` | 分数管理 |
| `StorageManager` | 本地存储 |
| `InputHandler` | 输入处理 |
| `UIRenderer` | UI渲染 |

## 🎯 游戏规则

1. 使用方向键或 WASD 控制蛇的移动
2. 吃到食物获得 +10 分
3. 每 50 分提升一个等级（最高 10 级）
4. 等级越高，蛇移动速度越快
5. 撞到墙壁或自己的身体游戏结束
6. 蛇不能 180 度反向移动
7. 挑战并刷新你的最高分！

## 📜 项目规范

本项目遵循统一的开发规范，详细内容请查看 [CONTRIBUTING.md](./CONTRIBUTING.md)。

### 快速参考

**命名规范（帕斯卡命名法）：**
- 类名：`GameController`、`Snake`、`Food`
- 函数名：`StartGame()`、`UpdateScore()`、`RenderCanvas()`
- 变量名：`CurrentScore`、`GameState`、`SnakeBody`
- 常量：`CONFIG`、`MAX_LEVEL`、`SCORE_PER_FOOD`

**Commit 规范：**
```
<type>(<scope>): <subject>

类型：feat | fix | docs | style | refactor | perf | test | chore
```


## 🐛 问题反馈

如果发现任何问题，欢迎反馈！

## 📝 许可证

本项目仅供学习和娱乐使用。

---

🎮 祝你游戏愉快！
