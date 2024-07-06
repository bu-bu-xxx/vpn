#  vpn搭建

![vps搭建](./assets/vps_build.jpg)

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

# ssh证书申请

1. x-ui 申请ssh证书
2. 输入cloudfare托管的对应域名
3. 输入cloudfare的global api key
4. 输入注册的邮箱
5. 成功

global api key:`ded583f0b737b9ae43e7626b5b888e52b039d`

# vpn使用

* 安装v2ray工具

需要先安装v2ray内核，然后安装下面的GUI

安卓：<https://github.com/2dust/v2rayNG/releases>

windows：<https://github.com/2dust/v2rayN/releases/download/6.42/v2rayN-With-Core.zip>

ubuntu：<https://github.com/Qv2ray/Qv2ray?tab=readme-ov-file>

> **注意**：windows要下载v2rayN-With-Core.zip

* 添加节点

1. japan nat节点(推荐)

```
vmess://ewogICJ2IjogIjIiLAogICJwcyI6ICJKYXBuIiwKICAiYWRkIjogImphcGFuLmJ1YnVsYW1iLmxvbCIsCiAgInBvcnQiOiAzMzkwMywKICAiaWQiOiAiODhlMmNkZmEtOGViNC00NDE2LWM2OGUtZmFiMzFkMmI0NzMyIiwKICAiYWlkIjogMCwKICAibmV0IjogIndzIiwKICAidHlwZSI6ICJub25lIiwKICAiaG9zdCI6ICIiLAogICJwYXRoIjogIi84OGUyY2RmYSIsCiAgInRscyI6ICJub25lIgp9
```

或者

```
vmess://ewogICJ2IjogIjIiLAogICJwcyI6ICJKYXBhbi10Y3AiLAogICJhZGQiOiAiamFwYW4uYnVidWxhbWIubG9sIiwKICAicG9ydCI6IDMzOTA0LAogICJpZCI6ICIwMjRjYmY0NC0yMDI1LTQxNWItZDIwMC1hYjhiZDdlMDY0N2QiLAogICJhaWQiOiAwLAogICJuZXQiOiAidGNwIiwKICAidHlwZSI6ICJub25lIiwKICAiaG9zdCI6ICIiLAogICJwYXRoIjogIiIsCiAgInRscyI6ICJub25lIgp9
```

2. japan vps节点

```
vmess://ewogICJ2IjogIjIiLAogICJwcyI6ICJKYXBhbi1zbG93LXZwcyIsCiAgImFkZCI6ICIxMDMuNzYuMTMxLjIwNiIsCiAgInBvcnQiOiAxOTgxMiwKICAiaWQiOiAiOWIwZWM2ZjEtZWJhNC00ZWQwLWJhZDMtNjg2YmVmYWYzOTc5IiwKICAiYWlkIjogMCwKICAibmV0IjogIndzIiwKICAidHlwZSI6ICJub25lIiwKICAiaG9zdCI6ICIiLAogICJwYXRoIjogIi85YjBlYzZmMSIsCiAgInRscyI6ICJub25lIgp9
```

# 机场vpn购买

* fscloud

网站：`https://ginle1171.fsc.fscloud.cc/`

账号：`779117133@qq.com`

密码：`jjjj123456`

订阅链接：`http://fs123121.cdn.22.jiacdnd123456789.com/answer/land?token=ea88310021300916f9f282b52d4e39c9`

* kaochang

网站：`https://reborn.kaochang.ltd/`

账号：`779117133@qq.com`

密码：`jjjj123456`

订阅链接：`https://kaochang.cheap/api/v1/client/subscribe?token=37843a218f37806df93a380f86109c0a`

代理配置(可能，需要尝试)：

<img src="./assets/proxy1.png" alt="图1" style="zoom:50%;" />

<img src="./assets/proxy2.png" alt="图2" style="zoom:50%;" />
