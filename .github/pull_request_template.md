## 改动

复刻「拾野」生日蛋糕：黑底单层星空蛋糕、彩色流挂、玻璃穹顶、白盘蓝影、单根蜡烛与黄白火焰，配白色笔刷体 Happy birthday! 与拾野签名。打开即见，无需操作，纯静态 HTML / SVG / CSS / JS。

星点缓慢漂移闪烁，火焰循环缩放明灭；适配移动端安全区，并尊重系统减少动态设置。

## 合并后访问

预期 GitHub Pages URL：**https://cangwu-ai.github.io/birthday-cake-web/**

合并到 `main` 后，仓库 Settings → Pages → Build and deployment → Source 选择 **GitHub Actions**。`Deploy birthday cake to GitHub Pages` 工作流部署完成后可访问；实际链接以 Actions 的 `github-pages` environment URL 为准。当前 PR 不代表已经上线。

## 验证

- `node --check cake.js`。
- 具体已执行验证、截图和环境限制见 `docs/verification.md`。
- 合并后手机竖屏复核首屏动画、无横向滚动及资源加载。
