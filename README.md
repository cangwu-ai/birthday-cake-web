# 拾野 · 星空生日蛋糕

用纯静态 HTML、SVG、CSS 和少量 JavaScript 致敬抖音「拾野」生日蛋糕录屏。黑色全屏中呈现单层星空蛋糕、彩色霓虹流挂、白盘蓝影与玻璃穹顶，一根细奶油蜡烛轻轻明灭，穹顶星点缓慢漂移闪烁。

打开即见蛋糕动画，移动端优先，无开场按钮、音频或额外操作。系统开启「减少动态效果」时显示静态画面。插画为代码重绘，未将原录屏或参考截图作为网页背景。

## 访问与部署

合并至 `main` 后的预期地址：**https://cangwu-ai.github.io/birthday-cake-web/**

1. 仓库管理员在 **Settings → Pages → Build and deployment → Source** 选择 **GitHub Actions**。
2. 将本分支 PR 合并到 `main`。`.github/workflows/pages.yml` 自动打包并发布 `index.html`、`style.css`、`cake.js` 与 `assets/`，无需构建工具或后端。
3. 等待 **Actions → Deploy birthday cake to GitHub Pages** 成功；访问工作流 `github-pages` environment 给出的 URL。也可以通过 `workflow_dispatch` 手动发布当前 `main`。

此地址是部署目标，只有合并、启用 Pages 且工作流成功后才会生效；本地文件修改不会直接发布。仓库重命名或转移时，请同步更新文档中的地址。站点全部使用相对资源路径，支持 `/birthday-cake-web/` 项目子路径。

## 本地预览

无需安装依赖。在仓库根目录运行：

```sh
python3 -m http.server 8000
```

打开 <http://localhost:8000/>，在浏览器设备模式检查 390 × 844。也可直接打开 `index.html`；推荐通过静态服务器预览部署行为。

## 文件与验收

- `index.html`：可缩放蛋糕插画、穹顶、蜡烛和无障碍描述。
- `style.css`：全黑背景、安全区、响应式比例、循环动画与减少动态设置。
- `cake.js`：固定种子的彩色星点与纸屑，不使用外部库或网络请求。
- `assets/`：本地字体子集、字体许可与图标。
- `docs/verification.md`：已执行检查、环境限制、手机验收步骤。
- `.github/pull_request_template.md`：包含预期访问 URL 和部署步骤的 PR 模板。

字体为 Kaushan Script 和马善政毛笔楷书的字符子集，遵循 SIL Open Font License 1.1，许可与署名见 `assets/FONT-LICENSES.txt`。本作品是参考视觉的前端致敬，不代表原作者官方站点。
