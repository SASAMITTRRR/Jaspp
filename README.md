# Jaspp

macOS 菜单栏工具，提供风扇监控与温控曲线、局域网遥控、显示器亮度、Apple Music 控制和本机写信台。

## 下载

- 安装包：在 Releases 下载 `Jaspp-1.2.1-arm64.dmg`，拖入 Applications。
- 源码：下载本仓库的 `Jaspp-1.2.1-source.zip` 并解压，内含完整 Swift/Python/网页源码、构建脚本、测试及第三方许可证。
- 支持 Apple Silicon，macOS 14+，需要 `/usr/bin/python3`（Xcode Command Line Tools 提供）。

## 构建

解压源码，进入 Jaspp-source 文件夹，运行 `bash build.sh`。生成 `build/Jaspp.app`，构建时自动执行 56 项风扇逻辑检查。运行 `PYTHONDONTWRITEBYTECODE=1 python3 tests/test_mail.py` 可检查邮件配置逻辑，不会发邮件或控制硬件。

首次启用风扇控制需要管理员授权。邮件功能需要使用者自己的 Resend 密钥和已验证域名。局域网遥控采用口令认证，仅用于受信任网络。

## 发布说明

此版本从清理后的源码重新构建，不包含作者的邮件记录、密钥、连接口令或个人域名；使用独立数据目录。第三方许可证保留。详见 `发布检查.txt`。

应用使用临时签名，未经过 Apple 公证，首次打开可能被 Gatekeeper 拦截；不同机型仍需自行验证。此发布验收没有执行真实风扇控制、发邮件或关机。
