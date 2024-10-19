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
