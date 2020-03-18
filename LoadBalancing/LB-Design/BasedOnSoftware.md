# 基于软件负载均衡

指使用软件的方式来分发和均衡流量，分为7层协议 和 4层协议。

## L7

基于第七层应用层来做流量分发的称为7层负载均衡。

最大的特点就是灵活，请求的 URL、Header 都是我们可以掌控的，
所以我们可以利用其中的任何信息为负载均衡策略所用

如：Nginx 反向代理。

## L4

基于第四层传输层来做流量分发的方案称为4层负载均衡。

当「Web 应用」所依赖的 TCP 协议的「服务」需要横向扩展，
或者需要做「数据库」、「分布式缓存」的多主、主从集群时。

如：LVS
