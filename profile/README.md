# HXC 1121

自建、自运维的代理订阅服务的基础设施代码：面板、节点、用户门户、计费与部署工具都在这里。

## 组成

| 层 | 内容 |
| --- | --- |
| 面板 | X-UI 管理面板（前后端分离）、Remnawave 面板（前端 / 后端） |
| 节点 | Remnawave 节点组件 |
| 用户门户 | 注册登录、仪表盘（余额 / 流量 / 到期 / 订阅链接）、余额购买套餐、个人中心 |
| 计费 | 基于 Xboard 的二次开发分支（MIT） |
| 工具 | 订阅聚合、部署与运维脚本 |
| 知识 | 工作区记忆与部署文档 |

## 公开项目

### [dynamic-sub-aggregator](https://github.com/HXC-1121/dynamic-sub-aggregator)

把多个 3X-UI 面板的动态节点聚合成一条订阅链接。

- 支持 VLESS / VMess / Trojan 节点聚合
- 按客户端 `email` 标识过滤节点，一条订阅分发给多个用户
- 透传 `Subscription-Userinfo`，Clash Verge / Mihomo Party / FlClash 里直接看到上下行用量与到期时间
- 按剩余流量、到期时间过滤重复与失效节点
- 附 Nginx 反向代理与 systemd 部署脚本

## 约定

- 各仓库独立维护，默认分支 `main`。
- 只提交 `.env.example` / `.sample` 之类的模板，真实凭证不入库。
