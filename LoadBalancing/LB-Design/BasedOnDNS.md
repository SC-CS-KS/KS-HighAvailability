# 基于 DNS 负载均衡

DNS 的本质是解决「domain name --> IP」。
DNS 的“智能解析”功能 可以做到 IP 的动态返回，起到了负载均衡的作用。

由于其本身是一个工作在 L3（网络层）的解决方案，所以无法对“端口”进行工作。

## 场景

在DNS服务器解析域名的时候，根据不同地理位置的用户返回不同的IP。
相当于实现了按照「就近原则」将请求分流了，既减轻了单个集群的负载压力，也提升了用户的访问速度。

## 优势

配置简单，实现成本非常低，无需额外的开发和维护工作。

## 缺点
```text
1. 当配置修改后，生效不及时。
DNS一般会有多级缓存，所以当我们修改了DNS配置之后，
由于缓存的原因，会导致IP变更不及时，从而影响负载均衡的效果。

2. 大多是基于地域或者干脆直接做IP轮询，没有更高级的路由策略。
```