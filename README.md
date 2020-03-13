# netty-pool-sampler
Start a Springcloud Gateway, use netty default connection pool elastic.
This sampler project has only one filter to sleep 550ms.
My test scenario: run with Jemter 300/400/500 Threads, http request to http://ip:port/status/200(In acturally route to http://httpbin.org/status/200)

Then type command in Linux server: 
```
[root@10 netty_pool_sampler]# ss -lnt|grep 8080
Recv-Q  Send-Q  Local Address Port
129     128      8080
```
My question is why Recv-Q is full, if my Netty pool configurations error?
