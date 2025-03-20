# 01-Nex

![image](https://github.com/user-attachments/assets/2110a663-a5ab-49ea-9bb1-c90e81b02f0e)

twitter：https://x.com/NexusLabs

第二期2月18日开启

### **1. 安装 Rust 和 Cargo**

在 macOS 上安装 Rust 和 Cargo，可以使用以下命令：

```bash
curl --proto '=https' --tlsv1.2 -sSf https://sh.rustup.rs | sh
```

安装过程中会提示是否继续安装，输入 `1` 以继续。

安装完成后，更新环境变量：

```bash
source $HOME/.cargo/env
```

验证 Rust 和 Cargo 是否安装成功：

```bash
cargo --version
rustc --version
```

---

### **2. 安装 Homebrew**

确保安装了 Homebrew（macOS 的包管理工具）。如果没有安装，可以运行以下命令：

```bash
/bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)"

```

安装完成后，更新 Homebrew：

```bash
brew update
```

---

### **3. 安装编译工具和依赖**

使用 Homebrew 安装 `gcc`、`make`、`pkg-config` 和 OpenSSL 开发包：

```bash
brew install gcc make pkg-config openssl
```

安装 Git：

```bash
brew install git
```

---

### **4. 安装 `protoc`**

使用 Homebrew 安装 Protocol Buffers 编译器 `protoc`：

```bash
brew install protobuf
```

验证 `protoc` 是否安装成功：

```bash
protoc --version
```

---

### **5. 运行 Nexus Network CLI 安装脚本**

运行 Nexus Network 的安装脚本：

1. 下载并切换到安装脚本所在的目录。
2. 如果脚本使用的是 `bash` 或类似环境，可以运行以下命令：
    
    ```bash
    install_nexus.sh
    ```
    
3. 根据脚本提示安装或配置。

如果安装脚本对 OpenSSL 或 `pkg-config` 的路径有要求，可以显式设置它们的路径。例如：

```bash
export PKG_CONFIG_PATH=$(brew --prefix openssl)/lib/pkgconfig
export PATH="/usr/local/bin:$PATH"

```
