# VSCode 使用

## 1. sftp 插件

```json
{
  "name": "name",
  "host": "ip",
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

## 2. python 插件

```json
"python.formatting.autopep8Args": [
    "--max-line-length=120",
]
```