# Claude Code 零基础入门教程，claude code 大陆如何使用，使用其他模型qwen/deepseek api 大模型
Claude Code使用教程：https://youtu.be/COQ2GPhxNbM

### 一、准备工作：
1、大陆需准备科学网络环境，可以使用 [Clash Verge](https://github.com/clash-verge-rev/clash-verge-rev/releases/latest) 或 [v2rayN](https://github.com/2dust/v2rayN/releases/latest) 等，配合
[机场网站>>](https://kjvm.github.io/kl) 或自建节点使用。

2、下载安装Node.js  [点击下载>>](https://nodejs.org/zh-cn/download)

3、下载安装Git  [点击下载>>](https://git-scm.com/install/windows)

### 二、安装 Claude Code：
- [Claude Code 官网>>](https://claude.com/product/claude-code)

- 添加环境变量，用户变量 - Path - 编辑<br>
C:\Users\用户名\.local\bin\

- 绕过校验<br>
.claude.json 编辑<br>
"hasCompletedOnboarding": true,

### 三、使用其他模型Qwen/Deepseek api：
- [Qwen](https://bailian.console.aliyun.com/)
- [Deepseek](https://platform.deepseek.com/usage)

### 四、Claude Code 接入大模型
1、将 Claude Code 对接 Qwen 模型<br>
打开命令行（Win+R 输入 cmd 回车）

    setx ANTHROPIC_API_KEY "API_KEY"
    setx ANTHROPIC_BASE_URL "https://dashscope.aliyuncs.com/apps/anthropic"
    setx ANTHROPIC_MODEL "qwen3.6-flash-2026-04-16"

2、将 Claude Code 对接 Deepseek 模型<br>
打开命令行（Win+R 输入 cmd 回车）

    setx ANTHROPIC_API_KEY "API_KEY"
    setx ANTHROPIC_BASE_URL "https://api.deepseek.com/anthropic"
    setx ANTHROPIC_MODEL "deepseek-v4-flash"

3、查看参数是否设置成功（注意要关闭 cmd 重新启动后输入）:

    echo %ANTHROPIC_API_KEY%
    echo %ANTHROPIC_BASE_URL%
    echo %ANTHROPIC_MODEL%


## Claude Code 对接本地模型，完全免费使用
视频教程：https://youtu.be/QcJQT5vfJ3w

1、启动 Ollama，运行模型
打开命令行（Win+R 输入 cmd 回车）

    ollama run qwen3.5:9b-q4_K_M


2、将 Claude Code 对接本地模型

    setx ANTHROPIC_API_KEY "ollama"
    setx ANTHROPIC_BASE_URL "http://127.0.0.1:11434"
    setx ANTHROPIC_MODEL "qwen3.5:9b-q4_K_M"

*模型名称需要和你当前运行的模型名称一致，运行"ollama list"可以查看模型列表。



