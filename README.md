# love-letter

一封会动的电子情书：Canvas 爱心树动画 + 打字机情书 + 「在一起第 N 天」实时计时器。纯静态单页，无构建、无依赖安装。

## 内容

| 文件 | 作用 |
| --- | --- |
| `love.html` | 页面入口，浏览器直接打开即运行 |
| `assets/js/love.js` | Canvas 爱心树绘制（心形隐函数、贝塞尔曲线、粒子生长） |
| `assets/js/build.js` | 分镜编排（Jscex 异步流程）；**顶部常量即计时器起点** |
| `assets/js/calculate.js` | 打字机逐字效果 + 纪念日计时器 |
| `assets/res/love.mp3` | 背景音乐（`love.html` 中的 `<audio>` 默认被注释） |
| `assets/js/jquery`、`assets/js/jscex` | 第三方库：jQuery 1.7.2、Jscex |

## 本地打开

直接用浏览器打开 `love.html`（建议 Chrome / Firefox，页面内也做了浏览器兼容提示）。

## 部署到 GitHub Pages

仓库 Settings → Pages → Source 选择 `main` 分支根目录，之后访问：

```
https://cnzeropro.github.io/love-letter/love.html
```

若希望根路径直接渲染，可把 `love.html` 重命名为 `index.html`（本地无任何文件引用它，改动成本很低）。

## 修改要点

| 想改什么 | 改哪里 |
| --- | --- |
| 情书文案与落款 | `love.html` 中 `#code` 区块 |
| 计时器起点 | `assets/js/build.js` 顶部的 `year` / `month` / `day` / `hour` / `minute` / `second` |
| 背景音乐 | 取消 `love.html` 里 `<audio>` 那一行的注释 |
| 配色与字体 | `assets/css/default.css` |

> 本仓库是个人纪念页面，其中的人物与日期信息请勿用于其他用途。
