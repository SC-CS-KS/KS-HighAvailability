# 限流  

## [WhatIs](WhatIs.md)

## [设计](design/README.md)

## 实现  

### 接入层限流

接入层通常是指流量的入口，主要的目的有：  
负载均衡、非法请求过滤、请求聚合、缓存、降级、限流、A/B测试、服务质量监控等。  

* [Nginx/OpenResty 限流](Nginx-Throttling.md)

* [Guava RateLimiter](https://github.com/SunnnyChan/sc.drill-code/blob/master/java/java-lib/Guava/RateLimiter.md)  

* 阿里开源的 Sentinel

* [Redis+Lua - 分布式应用限流](https://www.toutiao.com/i6684055284526088717/)
