# Git 下载、安装与配置（Windows + macOS）
> 官方网址、安装步骤、初始配置（含SSH）

## 1. 官方下载网址
1.1 官网主页
```
https://git-scm.com
```
1.2 Windows 专用下载页
```
https://git-scm.com/download/win
```
1.3 macOS 专用下载页
```
https://git-scm.com/download/mac
```

---

## 2. Windows 安装步骤
2.1 下载安装包
- 访问 1.2 链接，自动识别系统，下载 **64-bit Git for Windows Setup**（.exe）。


2.2 运行安装（全程默认，关键几步如下）
- 许可协议：直接 Next。

- 安装路径：建议非系统盘（如 D:\Git），**路径勿含中文/空格**。

- 组件选择：默认勾选（推荐勾选“Git Bash Here”右键菜单）。

- 环境变量：选择 **Git from the command line and also from 3rd-party software**（必选）。

- SSH 执行文件：默认 **Use the bundled OpenSSH**。

- HTTPS 传输：默认 **Use the Windows Secure Channel library**。

- 换行符：默认 **Checkout Windows-style, commit Unix-style line endings**。

- 其余默认，最后 Install → Finish。


2.3 验证安装
```bash
# 打开 Git Bash 或 CMD/PowerShell，输入
git --version
# 输出版本号（如 git version 2.54.0.windows.1）即成功
```

---

## 3. macOS 安装步骤（3 种方法）
### 方法一：Homebrew 安装（推荐，最新版）
3.1.1 安装 Homebrew（未装时）
```bash
/bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)"
```
3.1.2 安装 Git
```bash
brew install git
```
3.1.3 验证
```bash
git --version
```

### 方法二：Xcode 命令行工具（简单，版本略旧）
3.2.1 终端执行
```bash
xcode-select --install
```
3.2.2 弹窗点「安装」，完成后验证
```bash
git --version
```

### 方法三：官方 DMG 包（图形化）
3.3.1 访问 1.3 链接，下载 .dmg
3.3.2 双击打开，将 Git 拖入 Applications

3.3.3 验证
```bash
git --version
```

---

## 4. 全局基础配置（Windows + macOS 通用）
4.1 配置用户名（必设）
```bash
git config --global user.name "你的姓名"
```
4.2 配置邮箱（必设，与 GitHub 注册邮箱一致）
```bash
git config --global user.email "your-email@example.com"
```
4.3 查看全局配置
```bash
git config --global --list
```

---

## 5. 配置 SSH 密钥（免密登录 GitHub/GitLab）
5.1 生成密钥（一路回车，无需密码）
```bash
ssh-keygen -t ed25519 -C "your-email@example.com"
```
5.2 查看公钥（复制全部内容）
- Windows：`C:\Users\用户名\.ssh\id_ed25519.pub`
- macOS：`~/.ssh/id_ed25519.pub`
```bash
# macOS 终端直接查看
cat ~/.ssh/id_ed25519.pub
```
5.3 添加到 GitHub
- 登录 GitHub → Settings → SSH and GPG keys → New SSH key
- 粘贴公钥，保存即可。

---
