# Trae AI 配置
# 自动生成 Git Commit 时严格遵守以下规范

## Git Commit 规则（强制）

### 格式
```
<type>(<scope>): <description>
```

### 类型（type）只能用以下之一
- feat: 新功能、新模块
- fix: 修复 bug
- docs: 文档、注释变更
- style: 格式、空格、标点（不影响逻辑）
- refactor: 代码重构（非功能、非 bug）
- perf: 性能优化
- test: 新增/修改测试用例
- chore: 构建、配置、依赖、工具相关

### 作用域（scope）
- 写模块/文件名，如：spi、uart、main、utils
- 可省略：type: description

### 描述（description）
- 中文、小写开头、不超过 50 字
- 简洁说明做了什么

### 示例
- feat(spi): 实现基础读写接口
- fix(uart): 修复接收中断丢数据
- docs: 更新 README 接线说明
- chore: 升级编译器版本

### 本项目常用 scope
- game - 游戏核心逻辑
- snake - 蛇身相关
- food - 食物相关
- ui - 界面相关
- canvas - Canvas 渲染
- storage - 存储相关
- input - 输入处理
- readme - README 文档
- docs - 其他文档
- contributing - 贡献规范文档

## 命名规范（代码）
- 类名：帕斯卡命名法（PascalCase）
- 函数/方法名：帕斯卡命名法（PascalCase）
- 变量名：帕斯卡命名法（PascalCase）
- 常量：全大写+下划线（UPPER_SNAKE_CASE）

## 重要提示
- 自动生成 commit 必须严格遵守上述格式
- 只能使用规定 type，禁止随意用词
- 描述必须中文、简洁、准确
