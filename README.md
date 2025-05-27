# shadowsocks-rust

Shadowsocks-Rust 一键安装脚本, 全网唯一支持纯IPv4与IPv6网络vps的脚本。支持一键更新最新版本Shadowsocks-Rust

## 介绍

shadowsocks-rust 是 Shadowsocks 的一个 Rust 实现版本，相比原版具有以下优势：

- 高性能：Rust 语言的底层控制和零成本抽象带来卓越性能
- 低资源占用：内存占用少（运行时占用低于10m），适合在资源受限的 VPS 上运行
- 支持纯 IPv6：完整支持 IPv6 only 的 VPS 环境
- 稳定可靠：利用 Rust 的内存安全特性，减少崩溃和安全隐患
- 快速启动：服务启动迅速，配置简单

支持的加密方式：
- 经典加密：aes-256-gcm, aes-128-gcm, chacha20-ietf-poly1305 等
- AEAD 2022 加密：2022-blake3-aes-128-gcm, 2022-blake3-aes-256-gcm 等

## 系统要求

- CentOS / Rocky / AlmaLinux / Debian / Ubuntu
- 支持 x86_64, i686, arm, aarch64 架构
- 支持 IPv4, IPv6 或双栈网络环境

## 运行

一键安装：

```bash
wget --no-check-certificate https://raw.githubusercontent.com/athxx/shadowsocks-rust/main/ss-rust.sh && chmod +x ss-rust.sh && ./ss-rust.sh
```

**Docker版本** ( 无需预先安装Docker, 脚本自带安装 )
```bash
wget --no-check-certificate https://raw.githubusercontent.com/athxx/shadowsocks-rust/main/ss-rust-docker.sh && chmod +x ss-rust-docker.sh && ./ss-rust-docker.sh
```

## 功能

- 一键安装/更新/卸载
- 自动检测系统架构，下载对应版本
- 支持多种加密方式（包括 AEAD 2022）
- 自动配置 TCP Fast Open 以提高性能
- IPv4/IPv6 双栈支持
- 生成可分享的 SS 链接和二维码
- 系统服务集成（systemd）

## 使用方法

脚本提供直观的交互式菜单：

1. 安装 Shadowsocks Rust
2. 更新 Shadowsocks Rust
3. 卸载 Shadowsocks Rust
4. 启动服务
5. 停止服务
6. 重启服务
7. 修改配置（端口/密码/加密方式/TFO）
8. 查看当前配置
9. 查看服务状态

## 配置文件

安装完成后，配置文件位于 `～/.ss_config/config.json`

## 许可证

本项目基于 MIT 许可证开源，详见 [LICENSE](LICENSE) 文件。

