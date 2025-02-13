负载均衡支持创建 IPv6 NAT64 实例，腾讯云会给实例分配一个 IPv6 公网地址（即 IPv6 版的 VIP），该 VIP 会将来自 IPv6 客户端的请求转发给后端的 IPv4 云服务器。

## 什么是 IPv6 NAT64 负载均衡
IPv6 NAT64 负载均衡是基于 NAT64 IPv6 过渡技术实现的负载均衡器。通过 IPv6 NAT64 负载均衡器，后端云服务器无需做任何 IPv6 改造即可快速接入 IPv6 用户的访问。

## IPv6 NAT64 负载均衡架构
IPv6 NAT64 负载均衡的架构如下图所示。
![](https://main.qcloudimg.com/raw/caae8ad5e6a49ce24aeaa3fc0a6fd0c7.svg)
通过 IPv6 网络访问 IPv6 NAT64 负载均衡时，负载均衡能平滑地将 IPv6 地址转换为 IPv4 地址，适配原有的服务，快速实现 IPv6 的改造。

## IPv6 NAT64 负载均衡优势
腾讯云负载均衡在助力业务快速接入 IPv6 时具有如下优势：
- **快速接入：**秒级接入 IPv6，随买随用快速上线。
- **业务平滑过渡：**业务仅需改造客户端，无需改造后端服务，便可平滑接入 IPv6。IPv6 NAT64 负载均衡支持来自 IPv6 客户端的访问，并将 IPv6 报文转换成 IPv4 报文，后端云服务器上的应用程序无需感知 IPv6，仍以原有形式部署工作。
- **易于使用：**IPv6 NAT64 负载均衡兼容原 IPv4 负载均衡的操作流量，零学习成本，低门槛使用。

>!
>- IPv6 NAT64 负载均衡仅支持北京、上海、广州三个地域。
>- IPv6 NAT64 负载均衡不支持传统型负载均衡。
>- IPv6 NAT64 负载均衡不支持获取 Client IP。
>- 互联网 IPv6 网络大环境还处于建设初期，如出现线路访问不通的情况，请填写 [工单](https://console.cloud.tencent.com/workorder/category) 反馈，同时在内测期间，不提供 SLA 保障。

## 操作指南
### 创建 IPv6 NAT64 负载均衡
1. 登录腾讯云官网，进入 [负载均衡购买页](https://buy.cloud.tencent.com/lb)。
2. 实例类型选择【负载均衡】，IP 版本选择【IPv6 NAT64】，其他配置和普通实例配置相同。
3. 购买完成后，返回至 [负载均衡实例列表页](https://console.cloud.tencent.com/loadbalance/index?rid=1&forward=1)，即可查看已购的 IPv6 NAT64 负载均衡。
![](https://main.qcloudimg.com/raw/d55b34c80b12ac6effa806d969ef74a0.png)

### 使用 IPv6 NAT64 负载均衡
登录 [负载均衡控制台](https://console.cloud.tencent.com/loadbalance/index?rid=1&forward=1)，单击实例 ID，进入详情页，在“监听器管理”页面配置监听器、转发规则、绑定云服务器，详情请参见 [负载均衡快速入门](https://cloud.tencent.com/document/product/214/8975)。
![](https://main.qcloudimg.com/raw/37295edc8457d19babd3b6b9f2785de5.png)
