# Flask Babel

## 1. 命令

### 1.1. 抽取翻译文本

```bash
pybabel extract -F babel.cfg -k _l -o messages.pot .
```

### 1.2. 创建语言

```bash
pybabel init -i messages.pot -d app/translations -l zh
```

### 1.3. 编译

```bash
pybabel compile -d app/translations
```

### 1.4. 更新

```bash
pybabel extract -F babel.cfg -k _l -o messages.pot .
pybabel update -i messages.pot -d app/translations
```

## 2. 自定义命令

### 2.1. 初始化

```bash
flask translate init zh
```

### 2.2. 更新

```bash
flask translate update
```

### 2.3. 编译

```bash
flask translate compile
```
