---
name: WSL 与 Linux 命令速查
description: 在 Windows 上通过 WSL 操控 Linux 环境的常用命令、发行版管理与沙盒操作要点
---
# WSL 与 Linux 命令速查
## 发行版管理
- wsl --list --quiet：列出已安装发行版
- wsl --import <名称> <目录> <rootfs.tar.gz> --version 2：导入独立发行版
- wsl -d <名称> -e bash -lc "<命令>"：在指定发行版执行命令
## 常用排查
- 磁盘 df -h；内存 free -h；文件 find / -name "<名>"；文本 grep -rn "<词>" <目录>
- 进程 ps aux | head -30；端口 ss -tulpn
## 与 Windows 互操作
- Windows 盘挂载在 /mnt/c 等；wslpath -w/-u 转换路径
