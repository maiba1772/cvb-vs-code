# CVB Language - VS Code 语法高亮插件 🚀

[![GitHub](https://img.shields.io/badge/GitHub-Repository-blue.svg)](https://github.com/maiba1772/cvb)
[![Gitee](https://img.shields.io/badge/Gitee-Repository-red.svg)](https://gitee.com/maiba1772/cvb)
[![License](https://img.shields.io/badge/License-MIT-green.svg)](LICENSE)
[![Version](https://img.shields.io/badge/Version-1.0.0-orange.svg)](https://github.com/maiba1772/cvb/releases)

## 📖 项目简介

**CVB** 是一门现代化的脚本编程语言，具有简洁的语法和强大的功能。本项目提供 CVB 语言的 **VS Code 语法高亮插件**，为您的编码体验增添色彩！

### ✨ 特性亮点

- 🎨 **完整的语法高亮** - 支持所有 CVB 语言特性
- 🚀 **代码折叠** - 快速折叠函数、循环和条件语句
- 🔧 **智能提示** - 自动补全括号和引号
- 📝 **注释支持** - 块注释 `(# ... #)` 高亮
- 🐰 **精美图标** - 专属兔子 Logo
- 🌐 **开源免费** - MIT 许可证，完全免费使用

## 🎯 语言特性

CVB 语言具有以下独特优势：

### 1. 简洁的语法设计

```cvb
(# 这是注释 #)

(# 变量定义 - 使用 => 操作符 #)
name=>str&"CVB Language"
version=>int&1

(# 输出 - #前缀关键字 #)
#print=>str&"Hello, World!"
```

### 2. 类型提示系统

```cvb
(# 内置类型支持 #)
text=>str&"Hello"
number=>int&42
decimal=>float&3.14
items=>list&["a", "b", "c"]
data=>dic&{"key": "value"}
```

### 3. 强大的控制流

```cvb
(# If-Else 条件判断 #)
#if score >= 60:
  #print=>str&"Pass"
#else:
  #print=>str&"Fail"

(# While 循环 #)
#while TRUE=10:
  #print=>str&"Looping"

(# For 循环遍历 #)
#for item in items:
  #print=>str&item
```

### 4. 函数定义

```cvb
(# 函数定义 #)
#def greet(name):
  result=>str&"Hello, " + name
  #print=>str&result

(# 调用函数 #)
greet("World")
```

### 5. 丰富的内置模块

```cvb
(# 导入模块 #)
#import<file, math, random, net, shell>

(# 数学运算 #)
result=>math.sqrt(16)

(# HTTP 请求 #)
response=>net.get("https://api.example.com")

(# 执行系统命令 #)
output=>shell.exec("ls -la")
```

## 📦 安装方法

### 方式一：从 VSIX 文件安装（推荐）

1. **下载插件包**
   - 从 [GitHub Releases](https://github.com/maiba1772/cvb/releases) 下载最新的 `.vsix` 文件
   - 或从 [Gitee Releases](https://gitee.com/maiba1772/cvb/releases) 下载

2. **在 VS Code 中安装**
   - 打开 VS Code
   - 按 `Ctrl+Shift+X` 打开扩展面板
   - 点击右上角的 `...` 菜单
   - 选择 **"从 VSIX 安装..."**
   - 选择下载的 `.vsix` 文件
   - 点击安装

### 方式二：命令行安装

```bash
# 使用 VS Code CLI
code --install-extension cvb-language-1.0.0.vsix
```

### 方式三：从源码构建

```bash
# 克隆仓库
git clone https://github.com/maiba1772/cvb.git
cd cvb/vs\ code

# 安装打包工具
npm install -g @vscode/vsce

# 打包插件
vsce package

# 安装生成的 .vsix 文件
code --install-extension cvb-language-1.0.0.vsix
```

## 🎨 语法高亮预览

安装后，您的 CVB 代码将显示如下：

```cvb
(# CVB Language Example #)

#import<str, int, math>

#def calculate(x, y):
  sum=>int&x + y
  product=>int&x * y
  #print=>str&"Sum: " + sum
  #print=>str&"Product: " + product

calculate(10, 5)
```

### 高亮颜色说明

| 元素类型 | 颜色 | 示例 |
|---------|------|------|
| 关键字 | 🔵 蓝色 | `#print`, `#if`, `#def` |
| 类型 | 🟢 绿色 | `str`, `int`, `list`, `dic` |
| 字符串 | 🟡 黄色 | `"Hello World"` |
| 数字 | 🟣 紫色 | `123`, `3.14` |
| 运算符 | 🟠 橙色 | `=>`, `+`, `-`, `*`, `/` |
| 注释 | ⚪ 灰色 | `(# comment #)` |
| 函数名 | 🔴 红色 | `greet`, `calculate` |

## 🛠️ 功能特性

### 1. 语法高亮
- ✅ 所有 CVB 关键字
- ✅ 内置类型和模块
- ✅ 字符串和数字字面量
- ✅ 运算符和分隔符
- ✅ 函数定义和调用

### 2. 代码编辑辅助
- ✅ 自动闭合括号 `{}`, `[]`, `()`
- ✅ 自动闭合引号 `"`, `'`
- ✅ 代码折叠（函数、循环、条件）
- ✅ 括号匹配高亮

### 3. 语言配置
- ✅ 文件关联：`.cvb`
- ✅ 注释格式：`(# ... #)`
- ✅ 代码缩进：2 空格
- ✅ 词法模式：CVB

## 📁 项目结构

```
cvb/
├── vs code/                      # VS Code 插件目录
│   ├── package.json              # 插件配置文件
│   ├── cvb.tmLanguage.json       # 语法高亮规则
│   ├── cvb-language-configuration.json  # 语言配置
│   ├── README.md                 # 本文件
│   ├── images/
│   │   └── icon.png              # 插件图标
│   └── cvb-language-1.0.0.vsix   # 插件包
├── cvb-lang/                     # CVB 语言解释器
│   ├── main.go                   # 入口文件
│   ├── lexer/                    # 词法分析器
│   ├── parser/                   # 语法分析器
│   ├── ast/                      # 抽象语法树
│   ├── evaluator/                # 求值器
│   └── object/                   # 对象系统
└── README.md                     # 主项目说明
```

## 🚀 快速开始

### 1. 创建第一个 CVB 程序

创建 `hello.cvb` 文件：

```cvb
(# 第一个 CVB 程序 #)

name=>str&"World"
#print=>str&"Hello, " + name + "!"

(# 计算 #)
a=>int&10
b=>int&20
sum=>int&a + b
#print=>str&"Sum: " + sum
```

### 2. 运行程序

```bash
# 使用 CVB 解释器
cvb.exe hello.cvb

# 或使用 REPL 交互模式
cvb.exe
>>> name=>str&"Test"
>>> #print=>str&name
```

## 📚 文档资源

- 📘 [CVB 语言官方](https://github.com/maiba1772/cvb)
- 🔧 [VS Code 扩展开发文档](https://code.visualstudio.com/api)
- 💡 [语法高亮指南](https://code.visualstudio.com/api/language-extensions/syntax-highlight-guide)

## 🔧 开发指南

### 修改语法高亮规则

编辑 `vs code/cvb.tmLanguage.json` 文件，添加或修改语法匹配规则。

### 测试语法高亮

1. 打开 VS Code 扩展开发主机
2. 按 `F5` 启动调试
3. 在新窗口中打开 `.cvb` 文件测试

### 打包发布

```bash
# 更新版本号
# 编辑 package.json 中的 version 字段

# 打包
vsce package

# 发布到 VS Code Marketplace
vsce publish

# 发布到 Open VSX
ovsx publish
```

## 🤝 贡献指南

我们欢迎所有形式的贡献！

### 如何贡献

1. Fork 本仓库
2. 创建特性分支 (`git checkout -b feature/AmazingFeature`)
3. 提交更改 (`git commit -m 'Add some AmazingFeature'`)
4. 推送到分支 (`git push origin feature/AmazingFeature`)
5. 开启 Pull Request

### 报告问题

- 🐛 Bug 报告：[GitHub Issues](https://github.com/maiba1772/cvb/issues)
- 💡 功能建议：[GitHub Discussions](https://github.com/maiba1772/cvb/discussions)

## 📄 许可证

本项目采用 **MIT 许可证** - 查看 [LICENSE](LICENSE) 文件了解详情。

## 👥 作者

- **maiba1772** - [GitHub](https://github.com/maiba1772) | [Gitee](https://gitee.com/maiba1772)

## 🌟 特别感谢

感谢所有为 CVB 语言做出贡献的开发者们！

## 📊 项目状态

- ✅ 语法高亮 - 已完成
- ✅ 代码折叠 - 已完成
- ✅ 自动补全 - 已完成
- 🚧 代码片段 - 开发中
- 🚧 IntelliSense - 计划中
- 🚧 调试器 - 计划中

## 🔗 相关链接

- **GitHub 仓库**: https://github.com/maiba1772/cvb
- **Gitee 仓库**: https://gitee.com/maiba1772/cvb
- **VS Code Marketplace**: (即将发布)
- **Open VSX**: (即将发布)

## 📬 联系方式

如有问题或建议，请通过以下方式联系：

- 提交 Issue: [GitHub Issues](https://github.com/maiba1772/cvb/issues)
- 发送邮件：maiba1772@xxx.com

---

<div align="center">

**⭐ 如果这个项目对你有帮助，请给一个 Star 支持！⭐**

Made with ❤️ by the CVB Team

[返回顶部](#cvb-language---vs-code-语法高亮插件-)

</div>
