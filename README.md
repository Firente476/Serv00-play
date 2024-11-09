# serv00 上的一些应用，包括 vless/argo+vmess/vmess+ws/hy2/socks5/mtproto/alist/nezha探针 等, 自动化部署、批量保号、进程防杀、消息推送



## 前置工作

1. 一个 Serv00 帐号
2. 无需使用面板，选 1 安装 serv00-play 后，选 13 即可

## 安装说明

```s
bash <(curl -Ls https://raw.githubusercontent.com/frankiejun/serv00-play/main/start.sh)
```

## 变量说明

| 变量名          | 示例   | 备注                                     |
| --------------- | ------ | ---------------------------------------- |
| HOSTS_JSON      | 见示例 | 可存放 n 个服务器信息                    |


各主机保活时可不必输入消息通知参数，由 github 同一配置参数。



## action 保活内容

1.定时自动登录各个主机，起到保号作用(因 serv00 需要每 3 个月登录一次)  
2.执行兜底保活策略  
3.检查主机上保活用的 cronjob 是否被删，若被删重建保活 cronjob  
4.自动更新 serv00-play 代码  


## HOSTS_JSON 的配置实例

```js
 {
   "info": [
    {
      "host": "s2.serv00.com",
      "username": "kkk",
      "port": 22,
      "password": "fdsafjijgn"
    },
    {
      "host": "s2.serv00.com",
      "username": "bbb",
      "port": 22,
      "password": "fafwwwwazcs"
    }
  ]
}
```

## 安装说明视频

安装使用说明可以看[这里](https://youtu.be/bpYV8r85F-8)

临时隧道已失效，请使用固定隧道名，[如何申请固定隧道名](https://youtu.be/KyMvtWknu-k)


