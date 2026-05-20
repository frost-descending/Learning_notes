# Windows CMD 常见命令速查表

## 一、文件和目录操作

| 命令 | 功能说明 | 示例 |
|------|----------|------|
| `dir` | 列出当前目录下的文件和子目录 | `dir` |
| `cd` | 切换目录 | `cd C:\Windows`<br>`cd ..` 返回上级目录 如: cd /D D:\python_code | 
| `mkdir` / `md` | 创建新目录 | `mkdir myFolder` |
| `rmdir` / `rd` | 删除空目录 | `rmdir myFolder` |
| `del` / `erase` | 删除文件 | `del file.txt` |
| `copy` | 复制文件 | `copy source.txt dest.txt` |
| `xcopy` | 高级复制（可复制目录树） | `xcopy src dest /E` |
| `move` | 移动文件或目录 | `move file.txt D:\` |
| `ren` / `rename` | 重命名文件或目录 | `ren old.txt new.txt` |
| `type` | 显示文本文件内容 | `type readme.txt` |
| `find` | 在文件中搜索字符串 | `find "hello" file.txt` |


## 二、系统信息与管理

| 命令 | 功能说明 | 示例 |
|------|----------|------|
| `systeminfo` | 显示详细的系统配置信息 | `systeminfo` |
| `tasklist` | 显示当前运行的进程列表 | `tasklist` |
| `taskkill` | 终止进程 | `taskkill /PID 1234 /F` |
| `shutdown` | 关机/重启 | `shutdown /s /t 0` 立即关机<br>`shutdown /r /t 0` 立即重启 |
| `cls` | 清空屏幕 | `cls` |
| `exit` | 退出 CMD 窗口 | `exit` |
| `ver` | 显示 Windows 版本 | `ver` |

## 三、网络相关命令

| 命令 | 功能说明 | 示例 |
|------|----------|------|
| `ping` | 测试网络连通性 | `ping google.com` |
| `ipconfig` | 查看 IP 地址、MAC 地址等 | `ipconfig /all` |
| `tracert` | 跟踪路由路径 | `tracert google.com` |
| `netstat` | 显示网络连接、端口等 | `netstat -an` |
| `nslookup` | 查询 DNS 记录 | `nslookup example.com` |
| `arp` | 查看/修改 ARP 缓存 | `arp -a` |
| `route` | 操作网络路由表 | `route print` |

## 四、磁盘与文件系统

| 命令 | 功能说明 | 示例 |
|------|----------|------|
| `chkdsk` | 检查磁盘错误 | `chkdsk C:` |
| `diskpart` | 磁盘分区管理（交互式） | `diskpart` |
| `format` | 格式化磁盘 | `format D:` |
| `vol` | 显示磁盘卷标和序列号 | `vol C:` |
| `tree` | 以树形结构显示目录 | `tree` |

## 五、批处理常用命令

| 命令 | 功能说明 |
|------|----------|
| `echo` | 输出文本或开关回显（`echo off/on`） |
| `set` | 设置/显示环境变量 |
| `if` | 条件判断 |
| `for` | 循环执行命令 |
| `goto` | 跳转到指定标签 |
| `pause` | 暂停批处理执行 |
| `rem` | 添加注释 |

## 六、实用技巧

- **命令帮助**：`命令 /?`  
  例如：`copy /?`
- **查看历史命令**：按 `↑`/`↓` 键，或使用 `doskey /history`
- **重定向输出**：  
  `>` 覆盖写入文件，`>>` 追加到文件  
  例如：`dir > list.txt`
- **管道**：`|` 将前一个命令输出传递给下一个命令  
  例如：`ipconfig | find "IPv4"`