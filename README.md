# AgentHarbor Downloads

这里仅分发 AgentHarbor Agent 的编译安装包、SHA-256 和使用说明。产品源码保存在独立私有仓库，不需要取得源码权限即可安装。

## 一行安装

完整指南：https://agentharbor-web.pages.dev/install

macOS（Apple 芯片 / Intel）与 Linux x64：

```bash
curl -fsSL https://agentharbor-web.pages.dev/install.sh | bash
```

Windows x64 PowerShell：

```powershell
irm https://agentharbor-web.pages.dev/install.ps1 | iex
```

安装器自动选择平台、核对 SHA-256 并安装到用户目录。首次模型登录、身份配置和网页配对需要用户完成。升级前先结束任务并运行 `agentharbor-agent stop`，然后重复安装命令。

当前为预览版，Windows 未签名，macOS 未做 Apple 公证。Linux 目前验证 Ubuntu 24.04 x64，需要 glibc；不支持 Alpine/musl。安装器不关闭系统安全检查。

[下载版本](https://github.com/Victor-Sava/agentharbor-downloads/releases) · [打开工作区](https://agentharbor-web.pages.dev)

许可证与第三方归属随安装归档保留。
