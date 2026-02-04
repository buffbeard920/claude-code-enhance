# Claude Code Enhance

为 VSCode Claude Code 扩展添加代码高亮, LaTeX 公式渲染, UI 优化等功能.

## 功能特性

- **代码语法高亮** - Highlight.js, 支持 180+ 种语言
- **LaTeX 公式渲染** - KaTeX, 支持矩阵/分数/积分等
- **表格暗色主题** - 渐变表头, 悬停高亮, 圆角边框
- **代码自动换行** - 长命令行自动换行显示
- **滚轮缩放** - Ctrl + 滚轮缩放界面 (50%-200%)
- **列表样式修复** - 有序列表数字正常显示

## 兼容版本

- Claude Code Extension: **2.1.31**
- 平台: Windows (win32-x64), Linux (linux-x64)

## 安装

### 方式一: 补丁脚本 (推荐)

```bash
cd claude-code-enhance
node patch_extension.js
```

脚本会自动:
1. 查找已安装的 Claude Code 扩展
2. 复制 enhance.js 到扩展目录
3. 修改 CSP 策略允许加载 CDN 资源
4. 注入增强脚本

### 方式二: 手动安装

1. 复制 `webview/enhance.js` 到扩展的 `webview/` 目录
2. 修改 `extension.js` 中的 CSP 策略
3. 在 HTML 模板中注入 enhance.js 脚本标签

## 安装后

重载 VSCode 窗口: `Ctrl+Shift+P` → `Developer: Reload Window`

## 使用说明

### 滚轮缩放

- `Ctrl + 滚轮上` - 放大
- `Ctrl + 滚轮下` - 缩小
- 缩放范围: 50% - 200%
- 缩放比例自动保存

### LaTeX 公式

| 语法 | 类型 | 示例 |
|------|------|------|
| `$$...$$` | 块级公式 | `$$\sum_{i=1}^n i$$` |
| `$...$` | 行内公式 | `$x^2 + y^2$` |
| `\[...\]` | 块级公式 | `\[\int_0^1 x dx\]` |
| `\(...\)` | 行内公式 | `\(e^{i\pi} + 1 = 0\)` |

矩阵示例:
```latex
$$
\begin{pmatrix}
1 & 2 \\
3 & 4
\end{pmatrix}
$$
```

## 扩展更新后

Claude Code 扩展更新会覆盖补丁, 重新运行即可:

```bash
node patch_extension.js
```

## 项目结构

```
claude-code-enhance/
├── patch_extension.js  # 补丁脚本
├── webview/
│   └── enhance.js      # 增强脚本 (核心)
└── README.md
```

## 技术细节

### CSP 修改

补丁脚本修改以下 CSP 策略:

- `style-src`: 添加 `https://cdnjs.cloudflare.com`
- `script-src`: 添加 `https://cdnjs.cloudflare.com`
- `font-src`: 添加 `https://cdnjs.cloudflare.com data:`

### 外部依赖

- [Highlight.js](https://highlightjs.org/) 11.9.0 (vs2015 主题)
- [KaTeX](https://katex.org/) 0.16.9

## License

MIT
