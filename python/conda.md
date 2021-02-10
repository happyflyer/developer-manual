# conda 使用

## 1. 虚拟环境使用

### 1.1. 创建

```bash
conda create -n my_venv python=3.6
```

```bash
conda create -n my_venv python=3.6 numpy
```

```bash
conda env list
```

### 1.2. 切换

- Linux or MacOS

```bash
conda activate my_venv
```

```bash
conda deactivate my_venv
```

- Windows

```powershell
activate my_venv
```

```bash
deactivate my_venv
```

### 1.3. 删除

```bash
conda remove -n my_venv --all
```

### 1.4. 重命名

```bash
conda create -n hhh --clone my_venv
conda remove -n my_venv --all
```

## 2. 包管理

```bash
conda list
```

```bash
conda install package_name
```

## 3. [清华源](https://mirrors.tuna.tsinghua.edu.cn/help/anaconda/)

```bash
vim ~/.condarc
```

```yaml
channels:
  - defaults
show_channel_urls: true
default_channels:
  - https://mirrors.tuna.tsinghua.edu.cn/anaconda/pkgs/main
  - https://mirrors.tuna.tsinghua.edu.cn/anaconda/pkgs/free
  - https://mirrors.tuna.tsinghua.edu.cn/anaconda/pkgs/r
  - https://mirrors.tuna.tsinghua.edu.cn/anaconda/pkgs/pro
  - https://mirrors.tuna.tsinghua.edu.cn/anaconda/pkgs/msys2
custom_channels:
  conda-forge: https://mirrors.tuna.tsinghua.edu.cn/anaconda/cloud
  msys2: https://mirrors.tuna.tsinghua.edu.cn/anaconda/cloud
  bioconda: https://mirrors.tuna.tsinghua.edu.cn/anaconda/cloud
  menpo: https://mirrors.tuna.tsinghua.edu.cn/anaconda/cloud
  pytorch: https://mirrors.tuna.tsinghua.edu.cn/anaconda/cloud
  simpleitk: https://mirrors.tuna.tsinghua.edu.cn/anaconda/cloud
```

```bash
conda clean -i
```

## 4. 代理

```bash
vim ~/.condarc
```

```yaml
proxy_servers:
  http: http://代理服务器IP:端口
  https: https://代理服务器IP:端口
```

## 5. Windows 环境变量

```properties
C:\ProgramData\Anaconda3;
C:\ProgramData\Anaconda3\Library\mingw-w64\bin;
C:\ProgramData\Anaconda3\Library\usr\bin;
C:\ProgramData\Anaconda3\Library\bin;
C:\ProgramData\Anaconda3\Scripts;
```
