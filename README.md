# SALTWIND · 绿帆竞速

一个基于 Three.js 的浏览器 3D 驾船小游戏。驾驶绿帆船穿越潮汐，收集海面上的 5 个航标，完成一次轻量的开放水域航行体验。

## 在线体验

打开 GitHub Pages 或直接在本地启动静态服务器即可运行项目。

## 功能

- Three.js 实时渲染的低多边形海面与帆船
- 5 个可收集的绿色航标
- 航速、航向、风力和航标进度 HUD
- 鼠标拖动或键盘控制船只
- 响应式布局，支持桌面和移动端窗口
- “重置航程”按钮可恢复初始状态

## 操作方式

| 操作 | 作用 |
| --- | --- |
| `W` / `↑` | 加速 |
| `S` / `↓` | 减速 |
| `A` / `←` | 向左转向 |
| `D` / `→` | 向右转向 |
| `Space` | 稳帆并降低速度 |
| 鼠标拖动 | 直接调整航向 |
| 重置航程 | 恢复初始位置、速度和航标状态 |

收集全部 5 个航标后，状态栏会显示 `LANDFALL`。

## 本地运行

项目是无需构建工具的静态网页，Three.js 通过 jsDelivr CDN 加载。

```bash
# 安装依赖（仅用于运行检查脚本）
pnpm install

# 启动一个本地静态服务器（任选其一）
pnpm dlx serve .
# 或
python -m http.server 8000
```

然后访问终端显示的本地地址。直接双击 `index.html` 也可以打开页面，但部分浏览器对 ES Module 的本地文件加载有限制，推荐使用静态服务器。

## 项目结构

```text
├── index.html   页面结构与 HUD
├── game.js      Three.js 场景、船只、航标和交互逻辑
├── styles.css   页面视觉样式与响应式布局
├── package.json npm 脚本与项目信息
└── 项目介绍与实施计划.docx  项目说明文档
```

## 开发检查

```bash
npm test
```

该命令会使用 Node.js 检查 `game.js` 的语法。

## 技术栈

- HTML5 / CSS3 / JavaScript ES Modules
- [Three.js](https://threejs.org/)
- [jsDelivr](https://www.jsdelivr.com/) CDN
