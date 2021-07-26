生成PACKAGE
===

该项目的主要内容是：生成`cmake`可以找到的`package`，并使用代码去使用该`package`

# 1.目录结构

`/myapp.cpp`：该源代码用于测试创建的`package`是否可以正常使用

`/mylib/`：该文件夹表示用于创建`package`

`/doc/`：过程构建以及一些说明文档

# 2.使用方式

## 2.1.构建`package`

在`package_make/mylib/`路径下：

```bash
mkdir build
cmake ..
make
make install
```

## 2.2.使用创建的`package`

在`package_make/`路径下：

```bash
mkdir build
cmake ..
make
```

