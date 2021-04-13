# study


## git clone 报错  fatal: unable to access 'https://github.com/1217207804/study.git/': OpenSSL SSL_read: Connection was reset, errno 10054

>产生原因：一般是这是因为服务器的SSL证书没有经过第三方机构的签署，所以才报错  
参考网上解决办法：解除ssl验证后，再次git即可
```
git config --global http.sslVerify "false"
```

