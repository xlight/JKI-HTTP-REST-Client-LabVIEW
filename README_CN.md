[![Image](https://www.vipm.io/package/jki_lib_rest_client/badge.svg?metric=installs)](https://www.vipm.io/package/jki_lib_rest_client/)
[![Image](https://www.vipm.io/package/jki_lib_rest_client/badge.svg?metric=stars)](https://www.vipm.io/package/jki_lib_rest_client/)
![LabVIEW Version](https://img.shields.io/badge/LabVIEW-2020-%23E37725.svg?})
![OS](https://img.shields.io/badge/OS-Windows-%2353E020.svg?})
![OS](https://img.shields.io/badge/OS-Mac-%2353E020.svg?})
![OS](https://img.shields.io/badge/OS-Linux-%2353E020.svg?})


![HTTP REST Client for LabVIEW](https://user-images.githubusercontent.com/381432/194727878-ed7f915e-dd36-4e6e-a8ad-6088125d2c50.png)
# LabVIEW HTTP REST Client

HTTP REST Client for LabVIEW 最初由 [JKI](https://jki.net) 创建，是一个用于将 LabVIEW 应用程序与 RESTful Web 服务连接的 HTTP 客户端库。
HTTP REST Client 提供了 HTTP 协议的客户端实现，专为集成 LabVIEW 应用程序与 Web 服务而设计。
REST Client 增强了 LabVIEW 原生的 HTTP 实现，添加了几个功能，使其比 LabVIEW 原生 HTTP 客户端更适合连接 RESTful Web 服务。

想讨论 HTTP Rest Client？[加入社区讨论论坛](https://forums.jki.net/forum/68-http-rest-client/)。

## 安装

您可以通过 VI Package Manager 下载并安装 HTTP REST Client。

[获取 HTTP REST Client](https://www.vipm.io/package/jki_lib_rest_client/)

## 使用方法
HTTP REST Client 是一个 LabVIEW 工具包，提供了用于将 LabVIEW 应用程序与基于 REST 的 Web 服务连接的 VI 库。

### 调色板
要使用 HTTP REST Client，您需要将相应的 HTTP REST Client VI 拖放到程序框图中。
HTTP REST Client VI 位于 JKI Tools 函数调色板菜单下。

![函数调色板](https://raw.githubusercontent.com/xlight/JKI-HTTP-REST-Client-LabVIEW/refs/heads/master/img/rest-palette.png "函数调色板")

### 基本工作流程
该工具包提供了用于将 LabVIEW 应用程序与 RESTful Web 服务连接的 VI。基本工作流程如下图所示。

![基本工作流程](https://raw.githubusercontent.com/xlight/JKI-HTTP-REST-Client-LabVIEW/refs/heads/master/img/open-get-close.png "基本工作流程")

## API 参考

### 主调色板

![REST Client 调色板](https://raw.githubusercontent.com/xlight/JKI-HTTP-REST-Client-LabVIEW/refs/heads/master/img/rest-palette-open.png "REST Client 调色板")

#### 创建 REST Client
创建 REST Client 实例。

![创建 REST Client](https://raw.githubusercontent.com/xlight/JKI-HTTP-REST-Client-LabVIEW/refs/heads/master/img/create-rest-client.png "创建 REST Client")

该 VI 提供多个参数用于定义如何创建 JKI REST Client 实例。

**基础 URL** 指定用于 HTTP 请求的基础 URL。

**转义 URL** 当为 true 时，指示 REST Client 在执行请求前转义所有 URL。如果您已经转义了 URL，请将此项设置为 false。

**身份验证** 允许为使用 HTTP 身份验证的服务设置用户名和密码。

**验证服务器** 当为 true 时，指示 REST Client 在使用 HTTPS 协议时验证服务器的证书。

**默认标头** 指定用于每个请求的标头数组。默认为 application/json 内容类型。

**Cookie 文件** 指定用于 cookie 的文件路径。

#### HTTP HEAD
执行 HTTP HEAD 请求。

![HTTP HEAD](https://raw.githubusercontent.com/xlight/JKI-HTTP-REST-Client-LabVIEW/refs/heads/master/img/http-head.png "HTTP HEAD")

该 VI 提供多个参数用于定义如何执行 HTTP 请求。

**路径** 指定用于 HTTP 请求的基础 URL 之下的路径。

**请求特定标头** 指定用于此特定 HTTP 请求的标头数组。
创建 JKI REST Client 时指定的默认标头与请求特定标头将一起用于 HTTP 请求。

#### HTTP GET
执行 HTTP GET 请求。

![HTTP GET](https://raw.githubusercontent.com/xlight/JKI-HTTP-REST-Client-LabVIEW/refs/heads/master/img/http-get.png "HTTP GET")

该 VI 提供多个参数用于定义如何执行 HTTP 请求。

**路径** 指定用于 HTTP 请求的基础 URL 之下的路径。

**请求特定标头** 指定用于此特定 HTTP 请求的标头数组。
创建 JKI REST Client 时指定的默认标头与请求特定标头将一起用于 HTTP 请求。

#### HTTP POST
执行 HTTP POST 请求。

![HTTP POST](https://raw.githubusercontent.com/xlight/JKI-HTTP-REST-Client-LabVIEW/refs/heads/master/img/http-post.png "HTTP POST")

该 VI 提供多个参数用于定义如何执行 HTTP 请求。

**路径** 指定用于 HTTP 请求的基础 URL 之下的路径。

**请求正文** 指定要发送到服务器的请求正文。

**请求特定标头** 指定用于此特定 HTTP 请求的标头数组。
创建 JKI REST Client 时指定的默认标头与请求特定标头将一起用于 HTTP 请求。

#### HTTP PUT
执行 HTTP PUT 请求。

![HTTP PUT](https://raw.githubusercontent.com/xlight/JKI-HTTP-REST-Client-LabVIEW/refs/heads/master/img/http-put.png "HTTP PUT")

该 VI 提供多个参数用于定义如何执行 HTTP 请求。

**路径** 指定用于 HTTP 请求的基础 URL 之下的路径。

**请求正文** 指定要发送到服务器的请求正文。

**请求特定标头** 指定用于此特定 HTTP 请求的标头数组。
创建 JKI REST Client 时指定的默认标头与请求特定标头将一起用于 HTTP 请求。

#### HTTP DELETE
执行 HTTP DELETE 请求。

![HTTP DELETE](https://raw.githubusercontent.com/xlight/JKI-HTTP-REST-Client-LabVIEW/refs/heads/master/img/http-delete.png "HTTP DELETE")

该 VI 提供多个参数用于定义如何执行 HTTP 请求。

**路径** 指定用于 HTTP 请求的基础 URL 之下的路径。

**请求特定标头** 指定用于此特定 HTTP 请求的标头数组。
创建 JKI REST Client 时指定的默认标头与请求特定标头将一起用于 HTTP 请求。

#### 销毁 REST Client
关闭 REST Client 实例并关闭所有打开的 HTTP 连接。

![销毁 REST Client](https://raw.githubusercontent.com/xlight/JKI-HTTP-REST-Client-LabVIEW/refs/heads/master/img/destroy-rest-client.png "销毁 REST Client")


### 响应标头调色板

![响应标头调色板](https://raw.githubusercontent.com/xlight/JKI-HTTP-REST-Client-LabVIEW/refs/heads/master/img/rest-palette-response-headers.png "响应标头调色板")

#### 按名称获取标头
通过名称获取响应 HTTP 标头值。

![按名称获取标头](https://raw.githubusercontent.com/xlight/JKI-HTTP-REST-Client-LabVIEW/refs/heads/master/img/get-header-by-name.png "按名称获取标头")

该 VI 提供以下参数。

**名称** 指定要获取的 HTTP 标头的名称。

#### 获取所有标头
获取所有响应 HTTP 标头。

![获取所有标头](https://raw.githubusercontent.com/xlight/JKI-HTTP-REST-Client-LabVIEW/refs/heads/master/img/get-all-headers.png "获取所有标头")




## 贡献

1. Fork 项目！
2. 创建您的特性分支：`git checkout -b my-new-feature`
3. 提交您的更改：`git commit -am 'Add some feature'`
4. 推送到分支：`git push origin my-new-feature`
5. 提交拉取请求

要为 JKI REST Client 做出贡献，您需要 32 位 LabVIEW 2013 f2 专业开发环境。

## 致谢

HTTP REST Client 是一个最初由 [JKI](http://jki.net) 创建并由社区维护的开源项目。

## 许可证

HTTP REST Client 在开源三条款 BSD 许可下分发，允许每个人使用和分发 HTTP REST Client 的源代码和编译版本。
有关详细信息，请参阅 [LICENSE.md](LICENSE.md) 文件。