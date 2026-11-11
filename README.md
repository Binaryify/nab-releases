# Nab

Nab 是一个下载管理器：多连接下载、断点续传，支持 HTTP(S)、FTP、磁力和种子、迅雷链接、网页视频（HLS）；浏览器扩展和内置浏览器会带上登录状态接管下载。它也是一个给人和 AI 用的命令行 `nab`。

这个仓库只放发布文件，从 [Releases](https://github.com/Binaryify/nab-releases/releases/latest) 下载。

## 桌面版

| 系统 | 下载 |
|---|---|
| macOS（Apple 芯片和 Intel） | `nab-<版本>.dmg` |
| Windows x64 | `nab-setup-<版本>-amd64.exe` |
| Linux x64 | `nab-<版本>-linux-amd64.tar.gz`（解开后运行 `install.sh`）或 `.deb` |

装好后会自己检查更新。

macOS 版目前还没有用 Apple 的开发者证书签名公证，第一次打开时系统会拦下：在“应用程序”里右键点 Nab，选“打开”；或者在终端运行

```shell
xattr -dr com.apple.quarantine /Applications/Nab.app
```

## 命令行 nab

装了桌面版的话，在「设置 → 命令行」点「安装 nab 命令」即可。服务器上单独使用，下载对应系统的 `nab-cli-<版本>-<系统>-<架构>`，解压后放进 PATH：

```shell
nab https://example.com/file.zip
nab probe --json <链接>
nab -h
```

每个文件的 SHA-256 在 `SHA256SUMS` 和 `SHA256SUMS-cli` 里。
