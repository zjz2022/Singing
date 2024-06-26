### http2 和 http1.1 有什么区别，如果有一段数据丢了会怎样

HTTP/2 与 HTTP/1.1 主要有以下几个区别：

1. 二进制传输：HTTP/2 采用二进制格式传输数据，改善了 HTTP/1.1 的易读性和可操作性的问题，提高了解析效率和网络传输效率。

2. 多路复用：HTTP/1.1 由于 TCP 的线头阻塞问题，导致同一时间只能完成一个请求。而 HTTP/2 采用了多路复用技术，通过在一个 TCP 连接中创建多个流（stream），每个流都有唯一的标识符和优先级，用于区分不同的请求/响应，这样就可以在同一连接下同时处理多个请求/响应，解决了线头阻塞的问题。

3. 首部压缩：HTTP/2 使用 HPACK 算法对请求和响应信息头进行压缩，降低了网络传输的数据量。

4. 服务器主动推送：HTTP/2 增加了服务器可以对客户端的推送，即一个响应可以对应多个请求，这对页面加载优化有很大的帮助。

如果在使用 HTTP/2 的情况下有一段数据丢了，HTTP/2 会通过 TCP 的重传机制保证数据的完整性。TCP 会跟踪哪些包已经被对方接收，如果有某个包在一定的时间内没有被对方确认接收，那么 TCP 会重新传输这个数据包。这样就保证了数据的可靠性。在这种情况下，由于 HTTP/2 的多路复用特性，丢失的数据包不会阻塞其他数据包的传输，所以它的性能仍然会优于 HTTP/1.1。