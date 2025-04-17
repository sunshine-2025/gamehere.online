# GameHere - 在线游戏平台

GameHere 是一个简洁、现代的在线游戏平台，提供多种类型的免费游戏。平台采用响应式设计，确保在各种设备上都能提供良好的游戏体验。

## 项目结构

```
GameHere/
├── index.html              # 主页面，展示游戏列表
├── assets/                 # 静态资源目录
│   └── images/            # 游戏预览图片
│       ├── escape-road-preview.jpg.png
│       ├── garden-bloom-preview.jpg.png
│       ├── bubble-tower-3d-preview.jpg.png
│       ├── Contract Deer Hunter.jpg.png
│       ├── Chess Online.png
│       └── Sprunki.png
├── games/                  # 游戏详情页面
│   ├── escape-road.html
│   ├── garden-bloom.html
│   ├── bubble-tower-3d.html
│   ├── contract-deer-hunter.html
│   ├── chess-online.html
│   └── sprunki.html
└── README.md               # 项目说明文件
```

## 技术栈

- HTML5
- Tailwind CSS (通过 CDN 引入)
- 响应式设计

## 页面结构

### 1. 主页 (index.html)
- 顶部导航栏：包含网站标题和主要导航链接（热门、趋势、新品、收藏）。
- 搜索框：用于搜索游戏。
- 用户相关按钮：通知和用户资料。
- 分类导航栏：包含游戏分类按钮（全部、动作、冒险、策略等）。
- 游戏卡片网格：动态展示所有游戏。
- 每个游戏卡片包含：
    - 游戏预览图 (点击可进入游戏页面)
    - 游戏类型标签
    - 游戏评分 (星级和数值)
    - 游戏标题
    - 简短描述
    - "Play Now" 链接提示
- 功能特性区域：展示平台特点（免费、即玩、新内容）。
- 页脚：包含关于、联系、条款、隐私等链接和版权信息。

### 2. 游戏详情页面 (games/*.html)
每个游戏详情页面都采用了统一的布局和风格：
- 动态背景效果。
- 返回主页按钮。
- 游戏区域：
    - 通过 `<iframe>` 嵌入外部游戏。
    - `sandbox` 属性用于限制 iframe 行为，防止意外跳转。
    - 游戏区域大小响应式调整。
- 游戏信息区域：
    - 游戏标题和描述。
    - 三栏信息卡片：
        - 关于游戏 (About the Game)
        - 如何玩 (How to Play)
        - 提示与技巧 (Tips & Tricks)
- 页脚：包含版权信息。

## 已实现游戏及 Iframe 链接

以下是当前版本包含的游戏及其在各自详情页面中的 iframe 链接：

1.  **Escape Road**
    - 类型：Racing
    - 页面：`games/escape-road.html`
    - Iframe 链接：`https://lagged.com/api/play/escape-road/`
    - 描述：在城市中进行刺激的驾驶冒险。

2.  **Garden Bloom**
    - 类型：Puzzle
    - 页面：`games/garden-bloom.html`
    - Iframe 链接：`https://www.bestgames.com/Garden-Bloom`
    - 描述：创造一个美丽的花园，看着它绽放。

3.  **Bubble Tower 3D**
    - 类型：Puzzle
    - 页面：`games/bubble-tower-3d.html`
    - Iframe 链接：`https://www.coolmathgames.com/0-bubble-tower-3d/play`
    - 描述：在这个 3D 泡泡射击游戏中瞄准并发射。

4.  **Contract Deer Hunter**
    - 类型：Action
    - 页面：`games/contract-deer-hunter.html`
    - Iframe 链接：`https://html5.gamedistribution.com/rvvASMiM/8c6960ab0b5141cf8115c43bffd90277/index.html`
    - 描述：体验在各种环境中狩猎鹿的刺激。

5.  **Chess Online**
    - 类型：Strategy
    - 页面：`games/chess-online.html`
    - Iframe 链接：`https://html5.gamedistribution.com/rvvASMiM/b80ebde6ee1b4adfaa96398a4261db80/index.html`
    - 描述：与来自世界各地的玩家在线对战国际象棋。

6.  **Sprunki**
    - 类型：Puzzle
    - 页面：`games/sprunki.html`
    - Iframe 链接：`https://cloud.onlinegames.io/games/2024/more2/sprunki/index.html`
    - 描述：一个有趣的益智游戏，通过匹配彩色球来挑战你的策略能力。

**注意:** Chess Online 的 iframe 链接为示例，实际嵌入可能需要不同的平台或实现方式。

## 开发历史概要

- **初始阶段**: 搭建项目基础结构，引入 Tailwind CSS，设计基本布局和样式。
- **游戏集成**: 逐步添加多个游戏（如 Escape Road, Garden Bloom, Bubble Tower 3D, Contract Deer Hunter, Chess Online），为每个游戏创建详情页面，并通过 iframe 嵌入。
- **界面优化**: 统一游戏详情页面的布局和样式，采用动态背景和信息卡片设计，增强视觉效果和用户体验。
- **功能完善**: 在首页添加了游戏分类筛选和搜索功能。
- **版本回退**:
    - 项目曾尝试集成 Sprunki 游戏并优化其界面，但遇到 iframe 跳转问题。
    - 为了解决此问题并恢复到稳定状态，项目代码已通过 `git reset --hard 7fccf1cb1b366699375b1ee19a38b22ec53c60cb` 回退到添加 Chess Online 游戏后的版本。
    - 已通过 `git push --force origin main` 将此回退同步到 GitHub 远程仓库。
    - 回退过程中发现并计划移除误添加的 `tatus` 文件。

## 后续建议

- **移除 tatus 文件**: 该文件与项目无关，应删除。
- **核对 Chess Online 链接**: 确认 `games/chess-online.html` 中的 iframe 链接是否为有效且可嵌入的链接。
- **重新评估 Sprunki 集成**: 如果仍需添加 Sprunki 游戏，需要找到可靠的嵌入源或处理 iframe 跳转问题。
- **代码清理**: 检查是否有因版本回退产生的冗余或未使用的代码/资源。
- **功能扩展**: 根据需要继续添加新游戏、用户系统或其他功能。

## 许可证
© 2024 GameHere - Level Up Your Gaming Experience! 