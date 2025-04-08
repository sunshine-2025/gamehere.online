# GameHere - 在线游戏平台

GameHere 是一个简洁、现代的在线游戏平台，提供多种类型的免费游戏。平台采用响应式设计，确保在各种设备上都能提供良好的游戏体验。

## 项目结构

```
GameHere/
├── index.html              # 主页面，展示游戏列表
├── assets/                 # 静态资源目录
│   └── images/            # 游戏预览图片
│       ├── escape-road-preview.jpg
│       ├── music-now-preview.jpg
│       └── archery-world-tour-preview.jpg
└── games/                 # 游戏详情页面
    ├── escape-road.html
    ├── music-now.html
    └── archery-world-tour.html
```

## 技术栈

- HTML5
- Tailwind CSS (通过 CDN 引入)
- 响应式设计

## 页面结构

### 1. 主页 (index.html)
- 导航栏：包含网站标题和导航链接
- 游戏卡片网格：展示所有可用游戏
- 每个游戏卡片包含：
  - 游戏预览图
  - 游戏标题
  - 游戏类型标签
  - 简短描述

### 2. 游戏详情页面
每个游戏页面都采用统一的布局结构：
- 返回按钮
- 游戏预览图和标题区域
- 游戏类型标签
- 3:1 布局的游戏区域和信息栏
  - 左侧：游戏 iframe
  - 右侧：游戏信息（关于、控制、特点、技巧）

## 已实现游戏

### 1. Escape Road
- 类型：Racing
- 描述：在城市中进行刺激的驾驶冒险
- 游戏链接：`https://1games.io/embed/escape-road-city-2`
- 特点：
  - 动态城市环境
  - 多个挑战关卡
  - 多种车辆可解锁

### 2. Music Now
- 类型：Music
- 描述：创作美妙的音乐，探索音乐世界
- 游戏链接：`https://html-classic.itch.zone/html/11407110/index.html`
- 特点：
  - 多种乐器选择
  - 直观的音乐创作界面
  - 实时播放功能

### 3. Archery World Tour
- 类型：Sport
- 描述：在世界各地测试你的射箭技巧
- 游戏链接：`https://play.famobi.com/archery-world-tour`
- 特点：
  - 全球多个地点
  - 天气效果
  - 特殊挑战模式

## 游戏 iframe 集成说明

为了确保游戏能够正常运行，我们使用了不同的游戏平台：

1. 1Games.io 平台
   - 用于 Escape Road 游戏
   - iframe 设置：
     ```html
     <iframe src="https://1games.io/embed/escape-road-city-2" 
             frameborder="0" 
             class="w-full min-h-[600px] lg:min-h-[700px]"
             allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" 
             allowfullscreen>
     </iframe>
     ```

2. Itch.io 平台
   - 用于 Music Now 游戏
   - iframe 设置：
     ```html
     <iframe src="https://html-classic.itch.zone/html/11407110/index.html" 
             frameborder="0" 
             class="w-full min-h-[600px] lg:min-h-[700px]"
             allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" 
             allowfullscreen>
     </iframe>
     ```

3. Famobi 平台
   - 用于 Archery World Tour 游戏
   - iframe 设置：
     ```html
     <iframe src="https://play.famobi.com/archery-world-tour" 
             frameborder="0" 
             class="w-full min-h-[600px] lg:min-h-[700px]"
             allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" 
             allowfullscreen>
     </iframe>
     ```

注意事项：
- 所有游戏使用统一的 iframe 样式设置
- 游戏区域采用响应式设计，在大屏幕上显示更大
- 已添加必要的权限设置，确保游戏功能正常运行

## 开发历史

### 第一阶段：基础架构
1. 创建项目基本结构
2. 设置 Tailwind CSS 配置
3. 创建统一的颜色方案和样式主题

### 第二阶段：游戏整合
1. 添加 Escape Road 游戏
   - 创建游戏详情页
   - 整合游戏 iframe
   - 添加游戏说明和控制指南

2. 添加 Music Now 游戏
   - 创建游戏详情页
   - 整合 itch.io 游戏框架
   - 添加音乐创作指南

3. 添加 Archery World Tour 游戏
   - 创建游戏详情页
   - 整合 Famobi 游戏框架
   - 添加射箭技巧指南

### 第三阶段：界面优化
1. 统一所有游戏页面的布局
   - 将游戏区域比例调整为 3:1
   - 优化游戏 iframe 的显示大小
   - 统一右侧信息栏的样式和内容结构

2. 改进用户体验
   - 简化游戏信息的展示
   - 优化控制说明的可读性
   - 添加清晰的游戏特点和技巧说明

## 待办事项
- [ ] 添加更多游戏
- [ ] 实现游戏搜索功能
- [ ] 添加用户评分系统
- [ ] 优化移动端体验
- [ ] 添加游戏分类筛选

## 贡献指南
1. Fork 本仓库
2. 创建新的功能分支
3. 提交您的更改
4. 推送到分支
5. 创建 Pull Request

## 许可证
© 2024 GameHere - Your Online Gaming Destination 