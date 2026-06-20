# Zhanyu-Scoop
<!-- [![en](https://img.shields.io/badge/lang-en-red.svg)](./README.bot.md) -->
[English](README.md) | [中文](README.zh.md)

---

scoop-zhanyu 是一个 scoop bucket,这个存储库是供个人使用的集合。

## 可用软件

此 bucket 包含以下应用程序的清单文件:

### 开发工具

| 类别     | 名称                                                            |
| -------- | --------------------------------------------------------------- |
| 编程语言 | go, nodejs, nodejs-lts, python, rustup-msvc                     |
| 编辑器   | neovim,  obsidian                                               |
| 终端     | powershell, powershell-lts, powershell-preview,windows-terminal |
| 字体     | JetBrains-Mono  Maple-Mono                                      |
| 开发工具 | git, jetbrains-toolbox, Rebased                                 |
| 其他     | scoop-search                                                    |

### 媒体娱乐

| 类别       | 名称                        |
| ---------- | --------------------------- |
| 播放器     | ffmpeg, potplayer, bilibili |
| 下载管理器 | Motrix-Next                 |
| 游戏平台   | steam                       |
| 加速器     | steampp                     |

### 实用生产

| 类别     | 名称                                                           |
| -------- | -------------------------------------------------------------- |
| 浏览器   | firefox-zh-cn, firefox-developer-zh-cn, googlechrome           |
| 办公套件 | libreoffice                                                    |
| 效率工具 | 7zip, snipaste, utools, windows-iso-downloader                 |
| 系统工具 | dark, auto-dark-mode, powertoys-np, wechat-np, qqnt, mobaxterm |
| 命令行   | scoop-search, sudo, winget                                     |

## 快速使用

### 安装Scoop

确保你已经允许 PowerShell 执行本地脚本。

```powershell
set-executionpolicy remotesigned -scope currentuser
```

Scoop安装到自定义位置

```powershell
$env:SCOOP='D:\scoop'
[environment]::setEnvironmentVariable('SCOOP',$env:SCOOP,'User')
Invoke-Expression (New-Object System.Net.WebClient).DownloadString('https://gh-proxy.org/https://get.scoop.sh')
```
如果无法下载可以尝试使用代理: `gh-proxy.org`

```http
# 原始链接
https://get.scoop.sh

# 代理链接
https://gh-proxy.org/https://get.scoop.sh
```

### 安装这个 Bucket

```bash
scoop bucket add zhanyu https://github.com/luigits/scoop-zhanyu
```

### 安装软件

```bash
# 安装指定软件
scoop install zhanyu/app_name

# e.g.
scoop install zhanyu/potplayer
```

### 卸载软件

```bash
# 卸载指定软件
scoop uninstall zhanyu/app_name

# e.g.
scoop uninstall zhanyu/potplayer
```

### 更新软件

```bash
# 假设scoop status 提示 potplayer 有更新。
scoop status

# 更新指定软件
scoop update zhanyu/app_name

# e.g.
scoop update zhanyu/potplayer
```

## 删除所有的 bucket

```bash
# 删除所有的 bucket
scoop bucket rm *

# 删除指定 bucket
scoop bucket rm zhanyu
```

## 常用命令

```bash
scoop update # 更新
scoop update * #更新所有软件
scoop install zhanyu/bilibli # 指定库安装指定软件
scoop install 7zip git --global # 全局安装7zip、git
scoop install python@3.12.4 # 安装指定版本的python
scoop cache rm * # 清楚所有的缓存
scoop cleanup * # 清理所有的旧版本应用

# 更新 scoop
scoop update

# 更新所有软件
scoop update *

# 指定库安装指定软件
scoop install zhanyu/bilibli

# 全局安装
scoop install 7zip git --global

# 清理缓存
scoop cache rm *

# 清理旧版本应用
scoop cleanup *
```
> [!warning]
> 软件自定义配置、文档等不建议放置在软件目录下。
>
>使用清理缓存命令会将其删掉，造成成果丢失，若执意如此，请备份到远程存储。

## 常用桶

```powershell
# 中国国内镜像bucket
# main: 官方维护的主库，主要是CLI程序
scoop bucket add main https://gitee.com/scoop-installer/Main

# extras: 官方维护的扩展库，包含GUI程序
scoop bucket add extras https://gitee.com/scoop-installer/Extras

# 字体库
# 推荐Maple Mo(编辑器中使用)、Maple Mono NF CN(包含图标、中文、日文字符的字体)
scoop bucket add nerd-fonts https://gitee.com/scoop-installer/scoop-nerd-fonts

# 高性能软件库
scoop bucket add dorado https://gitee.com/scoop-installer/dorado

# 非便捷程序
scoop bucket add nonportable https://gitee.com/scoop-installer/Nonportable
```

## 其他软件桶

[https://scoop.sh/#/buckets](https://scoop.sh/#/buckets)

[https://rasa.github.io/scoop-directory/by-score](https://rasa.github.io/scoop-directory/by-score)
