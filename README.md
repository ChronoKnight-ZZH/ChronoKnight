# ChronoKnight-ZZH.github.io

[![GitHub Pages](https://img.shields.io/badge/demo-online-brightgreen)](https://ChronoKnight-ZZH.github.io/)
[![GitHub last commit](https://img.shields.io/github/last-commit/ChronoKnight-ZZH/ChronoKnight)](https://github.com/ChronoKnight-ZZH/ChronoKnight)

这是我的第一个 GitHub 仓库，也是一个完全静态的**趣味网页合集**：把平时写着玩的小工具、小游戏和节日页面都放在这里，通过 GitHub Pages 直接在线访问。

**在线地址：<https://ChronoKnight-ZZH.github.io/>**

仓库根目录只放首页 `index.html`，其余子页面全部位于 `public/` 目录。

## 项目一览

### 实用工具

| 项目 | 说明 | 在线访问 |
| --- | --- | --- |
| MarkFlow | Markdown 阅读器，把纯文本渲染成阅读视图 | [MarkFlow](https://ChronoKnight-ZZH.github.io/public/MarkFlow.html) |
| LayUI 表单生成器 | 可视化搭表单，支持长短布局与代码格式化 | [Form Builder](https://ChronoKnight-ZZH.github.io/public/LayUI%20Form%20Builder.html) |
| HTML Playground | HTML / CSS / JS 在线运行工具 | [HTML Playground](https://ChronoKnight-ZZH.github.io/public/HTML%20Playground.html) |
| 静域密码 | 组合式密码生成器，特殊字符可选 | [index7](https://ChronoKnight-ZZH.github.io/public/index7.html) |
| Mermaid 本地查看器 | 粘贴 Mermaid 代码即时渲染图表（增强版） | [Mermaid](https://ChronoKnight-ZZH.github.io/public/Mermaid%20%E6%9C%AC%E5%9C%B0%E6%9F%A5%E7%9C%8B%E5%99%A8%20%C2%B7%20%E5%A2%9E%E5%BC%BA%E7%89%88.html) |
| 图片 API 调试 | 图片获取与切换 | [图片api](https://ChronoKnight-ZZH.github.io/public/图片api.html) |

### 游戏与视觉

| 项目 | 说明 | 在线访问 |
| --- | --- | --- |
| 魔方模拟器 | 在线 2 阶 ~ 12 阶魔方，可自由转动 | [CubeSim](https://ChronoKnight-ZZH.github.io/public/CubeSim.html) |
| 水果消消乐 | 简单易上手的方块消除小游戏 | [Fruit Match](https://ChronoKnight-ZZH.github.io/public/Fruit%20Match.html) |
| 围棋 19×19 | Suiji 围棋道场，带 AI 分析 | [围棋19x19](https://ChronoKnight-ZZH.github.io/public/围棋19x19.html) |
| 360° 全景预览 | 全景图片拖动浏览（含标记插件版本） | [panoramicViewer](https://ChronoKnight-ZZH.github.io/public/panoramicViewer.html) / [fullView](https://ChronoKnight-ZZH.github.io/public/fullView.html) |

### 页面实验

| 项目 | 说明 | 在线访问 |
| --- | --- | --- |
| Atelier | 商业空间规划原型 | [Atelier](https://ChronoKnight-ZZH.github.io/public/Atelier.html) |
| 冰箱管家 | Fridge Guardian 页面效果展示 | [FridgeGuardian](https://ChronoKnight-ZZH.github.io/public/FridgeGuardian.html) |
| 瀑布流图片 | 瀑布流布局，点击全屏弹窗查看 | [瀑布流图片](https://ChronoKnight-ZZH.github.io/public/瀑布流图片.html) |
| 节日页面 | 除夕、生日祝福动画页面 | [除夕快乐](https://ChronoKnight-ZZH.github.io/public/除夕快乐.html) · [生日快乐](https://ChronoKnight-ZZH.github.io/public/生日快乐.html) |

## 技术栈

- 纯 **HTML / CSS / JavaScript**，无需构建工具，双击即可运行
- 部分页面引入 [LayUI](https://layui.dev/)、Three.js 等第三方库
- 首页的项目列表由 `index.html` 内嵌的 JSON 数据驱动，增删页面只改数据即可
- 部署方式：[GitHub Actions](.github/workflows/static.yml) 自动发布到 GitHub Pages

## 目录结构

```
.
├── index.html              # 首页（内嵌站点数据，动态渲染导航）
├── README.md
├── public/                 # 所有子页面与静态资源
│   ├── MarkFlow.html
│   ├── LayUI Form Builder.html
│   ├── HTML Playground.html
│   ├── index7.html
│   ├── Mermaid 本地查看器 · 增强版.html
│   ├── 图片api.html
│   ├── CubeSim.html
│   ├── Fruit Match.html
│   ├── 围棋19x19.html
│   ├── panoramicViewer.html
│   ├── fullView.html
│   ├── Atelier.html
│   ├── FridgeGuardian.html
│   ├── 瀑布流图片.html
│   ├── 除夕快乐.html / 生日快乐.html
│   ├── style/              # 字体与图标等静态资源
│   └── app-debug.apk
└── .github/workflows/      # GitHub Pages 自动部署配置
```

## 新增页面

1. 把页面文件放到 `public/`
2. 打开 `index.html`，在顶部 `site-data` 中对应分区的 `items` 里加一条：

```json
{
  "name": "页面名称",
  "description": "一句话介绍",
  "href": "public/NewPage.html",
  "icon": "doc"
}
```

`icon` 取自同一份数据里的 `icons` 表，缺失时只是不显示图标。

## 本地运行

直接用浏览器打开 `index.html` 即可（路径都是相对路径）；也可以启动本地静态服务：

```bash
git clone https://github.com/ChronoKnight-ZZH/ChronoKnight.git
cd ChronoKnight
python -m http.server 8000
```

然后访问 <http://localhost:8000>。

## 说明

- 页面多为随手写的玩具项目，代码风格不统一，欢迎参考和提建议
- 文件名带空格或中文时，访问链接需要做 URL 编码

---

如果觉得有意思，欢迎点个 Star。
