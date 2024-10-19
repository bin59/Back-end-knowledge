# 下载并安装 Redis

下载 Redis for Windows：

Redis 官方并不直接支持 Windows，但有一个社区维护的版本。你可以从 MSOpenTech/Redis 下载 Windows 版本的 Redis。

选择一个适合你系统的版本（32 位或 64 位）并下载压缩包。

解压文件：
将下载的压缩包解压到一个目录，例如 C:\Redis。

配置 Redis

编辑配置文件：
打开 C:\Redis 目录，找到 redis.windows.conf 文件。
根据需要进行配置。例如，如果你想设置密码，可以添加或修改以下行：

```sh
requirepass your_redis_password
```

启动 Redis 服务
打开命令提示符：
按 Win + R 键，输入 cmd，然后按回车键打开命令提示符。
导航到 Redis 目录：
使用 cd 命令切换到 Redis 目录： cd C:\Redis

```sh
redis-server.exe redis.windows.conf
```

如果一切正常，你应该会看到 Redis 服务器启动的日志信息。
验证 Redis 服务
打开另一个命令提示符窗口：
再次按 Win + R 键，输入 cmd，然后按回车键打开一个新的命令提示符窗口。
连接到 Redis 服务器：
运行以下命令连接到 Redis 服务器：

```sh
     redis-cli.exe
```

如果你设置了密码，需要先进行身份验证：

```sh
auth your_redis_password
```

## window 重启 redis

```sh
net stop Redis
net start Redis
```

## 设置密码

修改 Redis 配置文件
找到 Redis 配置文件：

Redis 的配置文件通常位于 redis.windows.conf。默认路径可能是 C:\Program Files\Redis\redis.windows.conf。
编辑配置文件：

使用文本编辑器（如 Notepad++ 或 Visual Studio Code）打开 redis.windows.conf 文件。
找到 # requirepass foobared 这一行，去掉前面的 # 注释符号，并将 foobared 替换为您自定义的密码。例如：

```sh
requirepass your_strong_password
```

如果您在 Windows 系统上遇到 'redis-cli' 不是内部或外部命令，也不是可运行的程序或批处理文件 的错误，这通常是因为 redis-cli.exe 的路径没有添加到系统的环境变量中。

找到 redis-cli.exe 的路径：

默认情况下，redis-cli.exe 位于 Redis 安装目录下，例如 C:\Program Files\Redis。
添加路径到系统环境变量：

按 Win + X，选择“系统”。
点击“高级系统设置”。
在“系统属性”窗口中，点击“环境变量”按钮。
在“系统变量”部分，找到 Path 变量，然后点击“编辑”。
在“编辑环境变量”窗口中，点击“新建”，然后输入 redis-cli.exe 的路径，例如 C:\Program Files\Redis。
点击“确定”保存更改。
验证更改：

打开一个新的命令提示符窗口（按 Win + R，输入 cmd，按回车）。
输入 redis-cli，看看是否可以正常运行。
