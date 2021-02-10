# pip 使用

## 1. 包管理

```bash
pip install package_name
```

```bash
pip install package_name --timeout 600
```

```bash
pip install -r requirements.txt
```

```bash
pip freeze > requirements.txt
```

## 2. [清华源](https://mirrors.tuna.tsinghua.edu.cn/help/pypi/)

- 临时

```bash
pip install package_name -i https://pypi.tuna.tsinghua.edu.cn/simple
```

- 配置

```bash
vim ~/.config/pip/pip.conf
```

```properties
[global]
index-url = https://pypi.tuna.tsinghua.edu.cn/simple
```

## 3. 代理

- 临时

```bash
pip install package_name --proxy http://代理服务器IP:端口
```

- 配置

```bash
vim ~/.config/pip/pip.conf
```

```properties
[global]
proxy = http://代理服务器IP:端口
```

## 4. zeroc-ice 安装前的依赖

```bash
sudo apt-get install -y libssl-dev
sudo apt-get install -y libboost-all-dev
sudo apt-get install -y libbz2-dev
```

```bash
pip install zeroc-ice
```
