# FCM Hosts

Android 14+或某些时期可能需要这个

## 新方案

hosts方案有时候也会断连。现在推荐dns分流方案：

0. 如果以前设置过hosts，请删掉
1. 添加`geosite:googlefcm`策略，DNS使用国内doh服务。注意，无论你设置了`cn`还是`!cn`策略，保证它是最后一条
2. `proxy_group`中添加谷歌FCM，并设为直连

![image](https://github.com/user-attachments/assets/ca5e614e-9916-4193-938a-8da71b31962f)

## hosts方案

<details><summary>展开/收起</summary>

```
142.250.157.188     mtalk.google.com
74.125.200.188      alt1-mtalk.google.com
142.250.141.188     alt2-mtalk.google.com
64.233.171.188      alt3-mtalk.google.com
173.194.202.188     alt4-mtalk.google.com
74.125.126.188      alt5-mtalk.google.com
142.250.115.188     alt6-mtalk.google.com
108.177.104.188     alt7-mtalk.google.com
142.250.152.188     alt8-mtalk.google.com
180.163.151.161     dl.google.com
180.163.150.33      dl.l.google.com
```

如果你的手机上装了 Magisk，也可以考虑使用 [systemless-fcm-hosts](https://github.com/Goooler/systemless-fcm-hosts) 集成

## 规则订阅

https://gcore.jsdelivr.net/gh/entr0pia/fcm-hosts@fcm/fcm-hosts

https://github.com/entr0pia/fcm-hosts/raw/fcm/fcm-hosts

</details>



## 测试

可以使用 [FCM Toolbox](https://github.com/SimonMarquis/FCM-toolbox) 测试消息送达的情况

