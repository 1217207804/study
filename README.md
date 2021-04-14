# study


## git clone 报错  fatal: unable to access 'https://github.com/1217207804/study.git/': OpenSSL SSL_read: Connection was reset, errno 10054

>产生原因：一般是这是因为服务器的SSL证书没有经过第三方机构的签署，所以才报错  
参考网上解决办法：解除ssl验证后，再次git即可
```
git config --global http.sslVerify "false"
```
打印GC日志

```
# 必备
-XX:+PrintGCDetails
-XX:+PrintGCDateStamps
-XX:+PrintTenuringDistribution
-XX:+PrintHeapAtGC
-XX:+PrintReferenceGC
-XX:+PrintGCApplicationStoppedTime

# 可选
-XX:+PrintSafepointStatistics
-XX:PrintSafepointStatisicsCount=1

# GC日志输出的文件路径
-Xloggc:/path/to/gc-%t.log
# 开启日志文件分割
-XX:+UseGCLogFileRotation
# 最多分割几个文件，超过之后从头开始写
-XX:NumberOfGCLogFiles=14
# 每个文件上限大小，超过就触发分割
-XX:GCLogFileSize=100M

```

