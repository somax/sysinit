# SYSINIT

服务器必要环境的自动安装与部署工具，目前仅支持 Linux

## install
    git clone http://git.jkr3.com/somax/sysinit.git

## usage
    # sysinit <command> <params>

    # 初始化成全局命令
    ./sysinit init

    # 获取帮助
    sysinit help

    # 下载 node 二进制版本
    sysinit download-node <node-version>
    sysinit download-node v6.0.0

    # 下载 npm 包
    sysinit node-pack -g <package-names...> # 全局
    sysinit node-pack <package-names...> # 本地

    # 安装到远程电脑
    sysinit remote-install <user@remote-host> <node-version>
    sysinit remote-install user@192.168.123.110 v6.0.0


## tips
- 在执行远程安装之前，确保本机公钥已经`ssh-copy-id`到远程服务器上，可以避免输入密码的麻烦。