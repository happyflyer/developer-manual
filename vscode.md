# VSCode 使用

## 1. 基本配置

```json
{
  "editor.fontSize": 18,
  "editor.formatOnSave": false,
  "editor.rulers": [80, 100, 120, 160, 200, 240],
  "editor.tabSize": 4,
  "editor.wordWrap": "wordWrapColumn",
  "editor.wordWrapColumn": 220,
  "files.eol": "\n",
  "files.encoding": "utf8",
  "files.trimTrailingWhitespace": true,
  "terminal.integrated.fontSize": 20,
  "terminal.integrated.inheritEnv": false,
  "update.mode": "manual",
  "extensions.ignoreRecommendations": true,
}
```

## 2. 文件关联

```json
{
  "files.associations": {
    "*.json.template": "json",
    "sivas.config": "json",
    "global_sivas.config": "json",
    ".env": "properties",
    ".env.template": "properties",
    ".flaskenv": "properties",
    "nginx.conf": "NGINX",
    "supervisor.conf": "properties",
    "*.md": "markdown",
  },
}
```

## 3. 主题图标

- Atom One Dark Theme
- **Chinese (Simplified) Language Pack for Visual Studio Code**
- Material Icon Theme
- vscode-icons

```json
{
  "workbench.colorTheme": "Monokai",
  "workbench.iconTheme": "material-icon-theme",
}
```

## 4. 编辑效率

- Auto Close Tag
- Auto Rename Tag
- Beautify
- Better Comments
- **Bracket Pair Colorizer**
- Code Spell Checker
- Color Highlight
- EditorConfig for VS Code
- filesize
- Guides
- **indent-rainbow**
- Path Intellisense
- Polacode-2020
- **Prettier - Code formatter**
- Rainbow CSV
- Visual Studio IntelliCode
- XML Tools

```json
{
  "prettier.singleQuote": true,
  "prettier.endOfLine": "lf",
  "prettier.tabWidth": 2,
  "prettier.printWidth": 100,
}
```

## 5. [Sync 插件](https://www.cnblogs.com/lychee/p/11214032.html)

- **Settings Sync**

## 6. [SFTP 插件](https://blog.csdn.net/qq_41033254/article/details/107426206)

- SFTP

```json
{
  "name": "name_what_you_like",
  "host": "ip_address",
  "protocol": "sftp",
  "port": 22,
  "username": "username",
  "password": "password",
  "remotePath": "remotePath",
  "uploadOnSave": true,
  "ignore": [
    ".vscode",
    ".git",
    ".DS_Store",
    "**/__pycache__",
    "venv",
    "log",
    "tmp",
    "**/*.db",
    "**/*.mo",
    ".coverage",
    ".pytest_cache",
    ".env"
  ],
  "watcher": {
    "files": "**/*",
    "autoUpload": true,
    "autoDelete": true
  }
}
```

## 7. Python 相关

- Jupyter
- Pylance
- Python
- Python Docstring Generator
- Python Indent
- YAML

```json
{
  "python.formatting.autopep8Args": [
    "--max-line-length=120"
  ],
  "python.languageServer": "Pylance",
}
```

## 8. Flask 相关

- Better Jinja
- Jinja
- nginx.conf
- nginx.conf hint

## 9. JavaScript 相关

- ESLint
- JavaScript (ES6) code snippets
- jshint
- Sass/Less/Stylus/Pug/Jade/Typescript/Javascript Compile Hero Pro
- Vetur

```json
{
  "[javascript]": {
    "editor.tabSize": 2,
    "editor.defaultFormatter": "esbenp.prettier-vscode",
  },
  "[html]": {
    "editor.tabSize": 2,
    "editor.wordWrapColumn": 220,
    "editor.defaultFormatter": "esbenp.prettier-vscode",
  },
  "[css]": {
    "editor.tabSize": 2,
    "editor.defaultFormatter": "esbenp.prettier-vscode",
  },
}
```

## 10. Markdown 相关

- Markdown All in One
- Markdown PDF
- **Markdown Preview Enhanced**
- **Markdown Preview Github Styling**
- **Markdown TOC**
- markdownlint

```json
{
  "markdown-preview-enhanced.mermaidTheme": "default",
  "markdown-preview-enhanced.codeBlockTheme": "github.css",
  "markdown-toc.depthFrom": 2,
  "[markdown]": {
    "editor.tabSize": 2,
    "editor.wordWrapColumn": 220,
    "editor.defaultFormatter": "esbenp.prettier-vscode"
  },
}
```

## 11. Git 相关

- Git Graph
- Git History
- **GitLens — Git supercharged**

## 12. [TODO 插件](https://zhuanlan.zhihu.com/p/63303926)

- Todo Tree

```json
{
  "todo-tree.regex.regex": "((//|#|<!--|;|/\\*|^)\\s*($TAGS):|^\\s*- \\[ \\])",
  "todo-tree.general.tags": ["TODO", "FIXME", "BUG", "tag", "done", "note"],
  "todo-tree.regex.regexCaseSensitive": false,
  "todo-tree.tree.showInExplorer": true,
  "todo-tree.tree.showScanModeButton": true,
  "todo-tree.highlights.defaultHighlight": {
    "foreground": "white",
    "background": "yellow",
    "type": "tag",
    "icon": "check",
    "iconColour": "yellow",
    "rulerColour": "yellow"
  },
  "todo-tree.highlights.customHighlight": {
    "TODO": {
      "foreground": "black",
      "background": "yellow",
      "icon": "check",
      "iconColour": "yellow",
      "rulerColour": "yellow"
    },
    "FIXME": {
      "foreground": "black",
      "background": "grey",
      "icon": "beaker",
      "iconColour": "grey",
      "rulerColour": "grey"
    },
    "BUG": {
      "background": "red",
      "icon": "alert",
      "iconColour": "red",
      "rulerColour": "red"
    },
    "tag": {
      "background": "blue",
      "icon": "tag",
      "iconColour": "blue",
      "rulerColour": "blue",
      "rulerLane": "full"
    },
    "done": {
      "background": "green",
      "icon": "issue-closed",
      "iconColour": "green",
      "rulerColour": "green"
    },
    "note": {
      "background": "magenta",
      "icon": "note",
      "iconColour": "magenta",
      "rulerColour": "magenta"
    }
  },
}
```

## 13. [LaTeX 插件](https://zhuanlan.zhihu.com/p/43133114)

- LaTeX Workshop

```json
{
    "latex-workshop.latex.recipes": [
    {
      "name": "xelatex",
      "tools": ["xelatex"]
    },
    {
      "name": "pdflatex",
      "tools": ["pdflatex"]
    },
    {
      "name": "xe->bib->xe->xe",
      "tools": ["xelatex", "bibtex", "xelatex", "xelatex"]
    },
    {
      "name": "pdf->bib->pdf->pdf",
      "tools": ["pdflatex", "bibtex", "pdflatex", "pdflatex"]
    }
  ],
  "latex-workshop.latex.tools": [
    {
      "name": "xelatex",
      "command": "xelatex",
      "args": ["-synctex=1", "-interaction=nonstopmode", "-file-line-error", "-pdf", "%DOCFILE%"]
    },
    {
      "name": "pdflatex",
      "command": "pdflatex",
      "args": ["-synctex=1", "-interaction=nonstopmode", "-file-line-error", "%DOCFILE%"]
    },
    {
      "name": "bibtex",
      "command": "bibtex",
      "args": ["%DOCFILE%"]
    }
  ],
}
```
