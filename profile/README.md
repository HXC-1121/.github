# HXC 1121

自托管的网络基础设施小工具。解决的问题很窄：把已有的东西连起来，让流量和用量看得见。

## 项目

### [dynamic-sub-aggregator](https://github.com/HXC-1121/dynamic-sub-aggregator)

把多个 3X-UI 面板的动态节点聚合成一条订阅链接。

- 支持 VLESS / VMess / Trojan 节点聚合
- 按客户端 `email` 标识过滤节点，一条订阅分发给多个用户
- 透传 `Subscription-Userinfo`，Clash Verge / Mihomo Party / FlClash 里直接看到上下行用量与到期时间
- 按剩余流量、到期时间过滤重复与失效节点
- 附 Nginx 反向代理与 systemd 部署脚本

## 取向

自托管优先，依赖少，配置就是文件。项目还处在早期阶段，issue 和 PR 都欢迎。
