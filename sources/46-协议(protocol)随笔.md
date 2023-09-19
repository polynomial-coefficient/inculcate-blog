# 协议(protocol)随笔

<hr>

- 内网与外网(公网)一般是隔离的。

- 代理服务器可以创建 1 个连接内外网的通道。

- 代理服务器：视为应用层网关。

- socks protocol：约束内主机与代理服务器的通用标准，实现数据转发。

- socks5：工作在 transport layer 与 application layer 之间，提供了 1 种对 application layer 协议透明的代理服务器。当内主机与代理服务器完成 socks 握手之后，application layer 对代理服务器是无感知的。

<hr>

- example：

A(内) 与 B(外)，这 2 个进程之间进行 HTTP 通信，实际数据链路为：A->C->B， C：代理服务器。

但在这个过程中引入 socks5 protocol 之后，可以“欺骗”应用层的视角，令应用层的视角“认为”：整个通信过程仍旧是：A->B。
