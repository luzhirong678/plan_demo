# 项目全局规范

## 概述

本文档定义了本项目的所有开发规范，包括命名规范、代码风格、提交规范等。

## 1. 命名规范

### 1.1 JavaScript/TypeScript 命名

#### 类名（Class）
- **规范**：帕斯卡命名法（PascalCase）
- **规则**：每个单词首字母大写
- **示例**：
  ```javascript
  class GameController { }
  class Snake { }
  class Food { }
  class ScoreManager { }
  ```

#### 函数/方法名
- **规范**：帕斯卡命名法（PascalCase）
- **规则**：每个单词首字母大写
- **示例**：
  ```javascript
  StartGame()
  UpdateScore()
  RenderCanvas()
  CheckCollision()
  ```

#### 变量名
- **规范**：帕斯卡命名法（PascalCase）
- **规则**：每个单词首字母大写
- **示例**：
  ```javascript
  CurrentScore
  GameState
  SnakeBody
  FoodPosition
  ```

#### 常量
- **规范**：全大写 + 下划线分隔（UPPER_SNAKE_CASE）
- **规则**：所有字母大写，单词间用下划线分隔
- **示例**：
  ```javascript
  const CONFIG = {}
  const MAX_LEVEL = 10
  const SCORE_PER_FOOD = 10
  const GAME_STATES = {
    IDLE: 'idle',
    PLAYING: 'playing',
    PAUSED: 'paused',
    ENDED: 'ended'
  }
  ```

### 1.2 文件命名
- **规范**：帕斯卡命名法（PascalCase）或 短横线命名法（kebab-case）
- **示例**：
  - `GameController.js`
  - `snake-game.html`
  - `MainCanvas.js`

### 1.3 CSS 类名
- **规范**：短横线命名法（kebab-case）
- **示例**：
  ```css
  .game-container
  .score-panel
  .btn-primary
  ```

## 2. Git Commit 提交规范

### 2.1 强制格式

```
<type>(<scope>): <description>
```

### 2.2 类型（type）只能用以下之一

| 类型 | 描述 |
|------|------|
| feat | 新功能、新模块 |
| fix | 修复 bug |
| docs | 文档、注释变更 |
| style | 格式、空格、标点（不影响逻辑） |
| refactor | 代码重构（非功能、非 bug） |
| perf | 性能优化 |
| test | 新增/修改测试用例 |
| chore | 构建、配置、依赖、工具相关 |

### 2.3 作用域（scope）

- 写模块/文件名，如：spi、uart、main、utils
- 可省略：type: description

### 2.4 描述（description）

- 中文、小写开头、不超过 50 字
- 简洁说明做了什么

### 2.5 示例

```
feat(spi): 实现基础读写接口
fix(uart): 修复接收中断丢数据
docs: 更新 README 接线说明
chore: 升级编译器版本
```

### 2.6 本项目常用 scope

- `game` - 游戏核心逻辑
- `snake` - 蛇身相关
- `food` - 食物相关
- `ui` - 界面相关
- `canvas` - Canvas 渲染
- `storage` - 存储相关
- `input` - 输入处理
- `readme` - README 文档
- `docs` - 其他文档

### 2.7 本项目示例

```
feat(snake): 添加蛇身皮肤切换功能
fix(collision): 修复墙壁碰撞检测错误
docs(readme): 更新游戏玩法说明
style: 统一代码缩进为4个空格
refactor: 重构游戏状态管理
perf: 优化Canvas渲染性能
test: 添加蛇移动功能测试
chore: 更新项目依赖包
```

## 3. 代码注释规范

### 3.1 函数/方法注释
每个函数/方法前都应该有注释：

```javascript
/**
 * 初始化游戏控制器
 * @param {Object} Canvas - Canvas 元素
 * @returns {void}
 */
InitGame(Canvas) {
  // ...
}

/**
 * 更新游戏分数
 * @param {number} Points - 增加的分数
 * @returns {void}
 */
UpdateScore(Points) {
  // ...
}
```

### 3.2 复杂逻辑注释
复杂的代码片段需要注释：

```javascript
// 计算蛇的新位置并检测碰撞
// 1. 获取当前方向
// 2. 计算新的头部坐标
// 3. 检测墙壁碰撞
// 4. 检测自身碰撞
```

## 4. 代码风格规范

### 4.1 缩进
- 使用 4 个空格缩进
- 不要使用 Tab 字符

### 4.2 分号
- 语句结束必须加分号

### 4.3 大括号
- 大括号不换行

```javascript
// ✅ 正确
if (Condition) {
  // ...
}

// ❌ 错误
if (Condition)
{
  // ...
}
```

### 4.4 空行
- 函数之间留空行
- 逻辑块之间留空行

## 5. 文件结构规范

```
project/
├── src/
│   ├── components/
│   │   ├── GameController.js
│   │   ├── Snake.js
│   │   └── Food.js
│   ├── utils/
│   │   └── CollisionDetector.js
│   └── styles/
│       └── Main.css
├── docs/
│   └── PRD.md
├── index.html
└── README.md
```

## 6. 最佳实践

### 6.1 代码组织
- 一个文件只做一件事
- 保持函数简短（不超过 50 行）
- 合理拆分复杂逻辑

### 6.2 性能考虑
- 避免不必要的重绘
- 合理使用缓存
- 优化循环和递归

### 6.3 可维护性
- 保持代码清晰易读
- 及时重构糟糕的代码
- 删除无用的代码

## 7. 规范检查清单

- [ ] 类名使用帕斯卡命名法
- [ ] 函数/方法名使用帕斯卡命名法
- [ ] 变量名使用帕斯卡命名法
- [ ] 常量使用全大写+下划线
- [ ] Commit 消息符合规范（type: description）
- [ ] Commit 描述使用中文、小写开头
- [ ] Commit 描述不超过 50 字
- [ ] 函数/方法前有注释
- [ ] 复杂逻辑有注释
- [ ] 代码格式统一
