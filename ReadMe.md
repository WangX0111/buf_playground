# Buf.build Playgroud

## intro
buf.build可以替代protoc进行更工程化的proto管理

## 安装
```sh
# 下载 "https://github.com/bufbuild/buf/releases/download/v${VERSION}/buf-$(uname -s)-$(uname -m)"
BIN="/usr/local/bin" && \
sudo mv buf-Linux-x86_64 "${BIN}/buf" \
chmod +x "${BIN}/buf"
```

## 使用
### 初始化
```sh
# 初始化一个新的 Buf 项目
buf init
```
这将创建一个新的 buf.yaml 文件，该文件包含了 Buf 的配置信息。
buf.yaml里面应该包含有我们项目中需要使用的依赖。

### 定义proto
Buf 使用 Protobuf 文件（.proto 文件）作为输入，因此你需要创建一个或多个 Protobuf 文件来定义你的 API。例如，你可以创建一个名为 user.proto 的文件，并在其中定义一个简单的 gRPC 服务：

### 配置buf
接下来，你需要配置 Buf 以编译你的 Protobuf 文件。在你的项目根目录下创建一个名为 buf.gen.yaml 的文件，这里定义了如何编译你的proto文件


### 编译
现在，你可以使用以下命令编译你的 Protobuf 文件：
```sh
# 编译 Protobuf 文件
buf generate
```
