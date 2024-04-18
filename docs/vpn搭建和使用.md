#  vpn搭建

![vps搭建](./assets/vps搭建.jpg)

两种方法，通过cloudfare代理，可以增强安全性和连接速度（或许会提高速度）。

## vmess协议+ws传输

1. 进入vps，用`ssh -p <端口号> root@<IPv4地址>`
2. 安装x-ui，用`bash <(curl -Ls https://raw.githubusercontent.com/vaxilu/x-ui/master/install.sh)`
3. （可选）申请SSL证书：查看[x-ui的github官网](https://github.com/vaxilu/x-ui)里有SSL证书申请方法介绍
4. x-ui端口设置，注意购买的nat机器的端口范围是多少，端口设置成范围内
5. 登入x-ui面板

![image-20240416220235903](./assets/image-20240416220235903.png)

![image-20240416220636401](./assets/image-20240416220636401.png)

6. 把二维码拷贝下来，就可以用了

# vpn使用

* 安装v2ray工具

安卓：<https://github.com/2dust/v2rayNG/releases>

windows：https://github.com/2dust/v2rayN/releases/download/6.42/v2rayN-With-Core.zip

> 注意：windows要下载v2rayN-With-Core.zip

* 扫码添加节点

1. 安装后扫码

![](./assets/download.png)

或者添加

```
vmess://ewogICJ2IjogIjIiLAogICJwcyI6ICJ2bWVzcyt3c3w5RTVvLmxvdmVAeHJheS5jb20iLAogICJhZGQiOiAiWzJhMTI6YmVjMDoxNjg6NDg4OjpdIiwKICAicG9ydCI6IDU0ODUyLAogICJpZCI6ICI3ZGUyMDlkYS01OGVjLTQ1NDMtZTA1Yy00NjZlMWZjNjkzMmIiLAogICJhaWQiOiAwLAogICJuZXQiOiAid3MiLAogICJ0eXBlIjogIm5vbmUiLAogICJob3N0IjogIiIsCiAgInBhdGgiOiAiLzdkZTIwOWRhIiwKICAidGxzIjogIm5vbmUiCn0=
```

2. 扫码

![image-20240417231032972](./assets/image-20240417231032972.png)

或者添加

`````
vmess://ewogICJ2IjogIjIiLAogICJwcyI6ICJKYXBhbiIsCiAgImFkZCI6ICJbMmExMjpiZWMwOjE2NToxYjQ6Ol0iLAogICJwb3J0IjogMzM5MDQsCiAgImlkIjogImU5MDdiZWJhLTA1MTctNDMxMi1lNDBlLWU0ZDQ5NmFmYTE5NCIsCiAgImFpZCI6IDUsCiAgIm5ldCI6ICJ3cyIsCiAgInR5cGUiOiAibm9uZSIsCiAgImhvc3QiOiAiIiwKICAicGF0aCI6ICIvZTkwN2JlYmEiLAogICJ0bHMiOiAibm9uZSIKfQ==
`````

