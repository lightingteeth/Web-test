# Conda

## Conda 简介
Conda 是一个开源的包管理系统和环境管理系统，可以在 Windows、macOS 和 Linux 上使用。它可以用于安装、运行和更新包和它们的依赖项，以及在不同的项目之间切换环境。

Conda主要用于两个方面：管理包（即软件程序和它们所需的库）和管理环境。它是为了方便科学计算、数据科学、机器学习等领域设计的，但实际上任何人都可以使用它来管理软件包和环境。

## 为什么要使用 Conda？

- 环境隔离：你可以为不同的项目创建独立的环境。这意味着，不同项目所需的不同版本的软件包不会相互冲突。
- 易于安装和使用：Conda 使得安装和管理软件包变得非常简单，特别是在处理复杂的依赖关系时。
- 跨平台：Conda 在 Windows、macOS 和 Linux 上都可以使用。

## Conda 的基本概念

- 包（Package）：软件或库的集合。例如，Python 的一个库如 NumPy 就是一个包。
- 环境（Environment）：包含一组特定版本包的隔离空间。你可以有多个环境，每个环境可以有不同的包和不同的包版本。

## 安装 Conda
访问 [Conda 官网](https://www.anaconda.com/products/individual) 下载并安装 Anaconda 或 Miniconda。

或者使用一些包管理工具，详情见页面[包管理工具](../环境配置/配置工具.md)

## 基本命令

### 创建环境
```shell
conda create --name myenv python=3.8
```

### 激活和停用环境
激活环境：
```shell
conda activate myenv
```
停用环境：
```shell
conda deactivate
```

### 安装包
```shell
conda install numpy
```

### 列出环境和包
列出所有环境：
```shell
conda env list
```
列出环境中的包：

```shell
conda list
```

### 更新和删除包

更新包：

```shell
conda update numpy
```

删除包：

```shell
conda remove numpy
```

### 删除环境

```shell
conda env remove --name myenv
```

## 高级用法

### 环境导出和克隆

导出环境：

```shell
conda env export > environment.yml
```

克隆环境：

```shell
conda create --name myclone --clone myenv
```

### 使用 channels

```shell
conda install conda-forge::package-name
```

### 管理 Conda 配置

查看配置：

```shell
conda config --show
```

设置配置项：

```shell
conda config --set auto_activate_base false
```

---
更多详细信息，请访问 [Conda 文档](https://docs.conda.io/en/latest/).
