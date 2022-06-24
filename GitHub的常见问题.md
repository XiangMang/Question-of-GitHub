# GitHub的常见问题

## 问题1

`unable to access '[仓库网址]': Failed to connect to github.com port 443 after 21082 ms: Timed out`
解放方案：

```
git config --global --unset http.proxy 
git config --global --unset https.proxy
```

## 问题2

`OpenSSL SSL_read: Connection was reset, errno 10054`
解决方案：

```
git config --global http.sslVerify "false"
```

## 问题3

```
warning: ----------------- SECURITY WARNING ----------------
warning: | TLS certificate verification has been disabled! |
warning: ---------------------------------------------------
warning: HTTPS connections may not be secure. See https://aka.ms/gcmcore-tlsverify for more information.
```

解决方案：

```
git config --global http.sslVerify true
```

