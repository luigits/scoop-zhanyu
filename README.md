# Zhanyu-Scoop

[English](README.md) | [中文](README.zh.md)

---

scoop-zhanyu is a scoop bucket, and this repository is a collection for personal use.

## Available Software

This bucket contains manifest files for the following applications:

**Development Tools**

| Category              | Packages                                                        |
| --------------------- | --------------------------------------------------------------- |
| Programming Languages | go, nodejs, nodejs-lts, python, rustup-msvc                     |
| Editors               | neovim,  obsidian                                               |
| Terminals             | powershell, powershell-lts, powershell-preview,windows-terminal |
| Font                  | JetBrains-Mono  Maple-Mono                                      |
| Dev Tools             | git, jetbrains-toolbox,                                         |
| Other                 | scoop-search                                                    |

**Media & Entertainment**

| Category          | Packages                    |
| ----------------- | --------------------------- |
| Video Players     | ffmpeg, potplayer, bilibili |
| Download Managers | Motrix-Next                 |
| Game              | steam                       |
| Accelerate        | steampp                     |


**Utilities & Productivity**

| Category         | Packages                                                       |
| ---------------- | -------------------------------------------------------------- |
| Browser          | firefox-zh-cn, firefox-developer-zh-cn, googlechrome           |
| Office           | libreoffice                                                    |
| Tools            | 7zip, snipaste, utools, windows-iso-downloader                 |
| System Utilities | dark, auto-dark-mode, powertoys-np, wechat-np, qqnt, mobaxterm |
| CLI              | scoop-search, sudo, winget                                     |

**Frameworks & Runtime**

| Category     | Packages                                           |
| ------------ | -------------------------------------------------- |
| Runtime      | windowsdesktop-runtime, windowsdesktop-runtime-lts |
| AI/ML        | ollama                                             |
| Flutter      | flutter-cn                                         |
| Game Engines | godot                                              |

---

## Quick Start

### Install Scoop

Ensure PowerShell allows local script execution:

```powershell
set-executionpolicy remotesigned -scope currentuser
```

Install Scoop to custom location:

```powershell
$env:SCOOP='D:\scoop'
[environment]::setEnvironmentVariable('SCOOP',$env:SCOOP,'User')
Invoke-Expression (New-Object System.Net.WebClient).DownloadString('https://get.scoop.sh')
```

If the download fails, you can add proxy: `gh-proxy.org`.

```http
# Original link
https://get.scoop.sh

# Proxy link
https://gh-proxy.org/https://get.scoop.sh
```

### Add This Bucket

```bash
scoop bucket add zhanyu https://github.com/luigits/scoop-zhanyu
```

### Install Applications

```bash
# Install specific application
scoop install zhanyu/app_name

# e.g.
scoop install zhanyu/potplayer
```

### Uninstall Applications

```bash
# Uninstall specific application
scoop uninstall zhanyu/app_name

# e.g.
scoop uninstall zhanyu/potplayer
```

### Update Applications

```bash
# Suppose scoop status prompts potplayer for an update.
scoop status

# Update specific application
scoop update zhanyu/app_name

# e.g.
scoop update zhanyu/potplayer
```
### Remove Buckets

```bash
# Remove all buckets
scoop bucket rm *

# Remove specific bucket
scoop bucket rm zhanyu
```

### Common Commands

```bash
# Update scoop
scoop update

# Update all applications
scoop update *

# Install specific application from a bucket
scoop install zhanyu/bilibli

# Global install
scoop install 7zip git --global

# Clear cache
scoop cache rm *

# Cleanup old versions
scoop cleanup *
```

> [!warning] Warning
> It is not recommended to place the software customized configuration and documents in the software directory.
>
> Using the clear cache command will delete them, resulting in the loss of results. Otherwise, please back them up to remote storage.


## Other Buckets

[https://scoop.sh/#/buckets](https://scoop.sh/#/buckets)

[https://rasa.github.io/scoop-directory/by-score](https://rasa.github.io/scoop-directory/by-score)
