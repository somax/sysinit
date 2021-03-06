# SYSINIT

系统运行环境的安装与部署工具集

> 目前仅支持 Linux

## install

公司内网

    git clone http://git.jkr3.com/ops/sysinit.git

Github

    git clone https://github.com/somax/sysinit.git

## usage
    # 基本使用
    sysinit <command> <params>

    # 初始化成全局命令
    ./sysinit init

    # 获取帮助
    sysinit help

    # 查看远程可用 node 版本
    sysinit list-remote-node <filter-version>

    # 下载 node 二进制版本
    sysinit download-node <node-version>

    # 下载 npm 包
    sysinit node-pack -g <package-names...> # 全局
    sysinit node-pack <package-names...> # 本地

    # 安装到远程电脑, 如果不加 node-version 参数则只安装 npm-global 包
    sysinit remote-install <user@remote-host> [node-version]

    # 生成 nginx vhost 配置文件
    sysinit nginx-config <domain> <proxy-to>

## example
    sysinit download-node v6.0.0
    sysinit node-pack -g pm2 http-server
    sysinit list-remote-node v6
    sysinit download-node v6.6.0
    sysinit download-node v6.6.0 linux-armv71
    sysinit remote-install user@192.168.123.110 v6.0.0    

## tips
- 在执行远程安装之前，确保本机公钥已经`ssh-copy-id`到远程服务器上，可以避免输入密码的麻烦。


