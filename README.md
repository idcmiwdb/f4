# F4 Networks 裸金属服务器评测：$33/月起，免费 BGP Transit，纽约/堪萨斯城双机房

如果你在找一家能让你自带 IP 段、自由跑 BGP 的美国裸金属服务器，F4 Networks 这个名字可能比你想象的更值得认真看一眼。

价格不贵，起步 $33/月。机器是真物理机，不是什么 VPS 换皮。更关键的是：**所有套餐都免费附带 BGP Transit**，这在同价位里算是挺稀罕的事。

这篇文章把他们目前在售的套餐摸了个透，顺手也聊聊这家提供商到底适合谁。


---

## F4 Networks 是什么来头？

F4 Networks 是一家美国独立小型托管商，运营自己的 AS（AS21738），在堪萨斯城（Kansas City, MO）和纽约（Brooklyn, NY）各有一个机房。数据中心配备了 CCTV 监控和 24×7 现场安保人员，门禁走生物识别。

他们在 LowEndTalk 和 LowEndBox 这两个圈子里曝过光，反响不算差——主要受众是 BGP 爱好者、小型 ISP、以及需要跑自己 IP 段的技术型用户。有人评价说他们"新、积极、功能齐全"，机柜照片整洁有序，是那种让人觉得靠谱的小厂商风格。

👉 [浏览 F4 Networks 全部服务](https://store.f4.network/index.php/order/forms/a/NjAz)

---

## 堪萨斯城裸金属服务器

堪萨斯城是 F4 Networks 的主要机房，套餐选择最丰富，价格也是整个产品线里最实惠的起点。

| 套餐 | CPU | 内存 | 硬盘 | 流量 | 网速 | 月价 | 年价 | 下单 |
|------|-----|------|------|------|------|------|------|------|
| m1.medium | Intel Xeon E5-2620 v4 · 8核16线程 | 32 GB DDR4 ECC | 2×500 GB SSD | 100 TB | 10 Gbps | $54 | $594 | [ 立即订购](https://store.f4.network/index.php/order/main/packages/bare-metal-kc/a/NjAz) |
| m2.xlarge | 2×Intel Xeon Gold 6140 · 36核72线程 | 256 GB DDR4 ECC | 2×1 TB SSD | 300 TB | 10 Gbps | $234 | $2,574 | [ 立即订购](https://store.f4.network/index.php/order/main/packages/bare-metal-kc/a/NjAz) |
| m1.xxlarge | 2×Intel Xeon Platinum 8160 · 48核96线程 | 768 GB DDR4 ECC | 2×2 TB NVMe | 600 TB | 最高 40 Gbps | $699 | — | [ 立即订购](https://store.f4.network/index.php/order/main/packages/bare-metal-kc/a/NjAz) |

> 备注：m1.small、m1.small+、m1.large、m1.xlarge 目前显示 Out of Stock，如有需求可关注补货。

所有套餐均包含：IPv4 + IPv6 各一个、远程 Console 访问、免费 BGP Transit（AS54852）、支持 BYOIP（带自己的 IP 段）。

---

## 纽约城裸金属服务器

2024 年下半年 F4 Networks 新开的纽约（Brooklyn）机房，东海岸覆盖更好，适合对延迟有要求的业务场景。

| 套餐 | CPU | 内存 | 硬盘 | 流量 | 网速 | 月价 | 年价（省 1 个月） | 下单 |
|------|-----|------|------|------|------|------|------|------|
| m1.large+ | 2×Intel Xeon E5-2640 v4 · 20核40线程 | 128 GB DDR4 ECC | 2×1 TB SSD | 60 TB | 10 Gbps | $152 | $1,672 | [ 立即订购](https://store.f4.network/index.php/order/main/packages/bare-metal-nyc/a/NjAz) |
| m1.xlarge+ | 2×Intel Xeon E5-2690 v4 · 28核56线程 | 256 GB DDR4 ECC | 2×1 TB SSD | 100 TB | 10 Gbps | $199 | $2,189 | [ 立即订购](https://store.f4.network/index.php/order/main/packages/bare-metal-nyc/a/NjAz) |

> 年付方案相当于第 12 个月免费，以 m1.xlarge+ 为例，年付比月付累计省下 $199。

纽约机房同样标配远程 Console、BGP Transit（免费）、IPv4 + IPv6，支持 BYOIP。

👉 [查看纽约服务器套餐](https://store.f4.network/index.php/order/main/packages/bare-metal-nyc/a/NjAz)

---

## BGP IP Transit — 单独购买也可以

如果你自己有服务器但缺一条干净的上游链路，F4 Networks 也单独卖 BGP Transit。

| 套餐 | 带宽 | 上游 | 月价 | 年价 |
|------|------|------|------|------|
| Premium 100M Transit | 不限量 100 Mbps | AS21738（多上游） | $39.95 | $439.45 |
| Premium 1G Transit | 不限量 1 Gbps | AS21738（多上游） | $149.95 | — |
| Premium 10G Transit | 不限量 10 Gbps | AS21738（多上游） | $849.95 | — |
| Cogent AS174 直连 | 1G on 10G | Cogent | $289 | — |
| Arelion AS1299 直连 | 1G on 10G | Arelion/Telia | $355 | $3,905 |
| GTT AS3257 直连 | 1G on 10G | GTT | $355 | — |

Premium 系列通过 AS21738 宣告，上游包括 Arelion/Telia AS1299、AT&T AS7018、Hurricane Electric AS6939、Cogent AS174、GTT AS3257，支持 Full/Partial/Default 表，全 BGP Community 支持，以及 RTBH（远程触发黑洞）。

传输方式灵活：GRE 隧道、WireGuard 隧道、专用机器/VPS BGP Transit 或直连 XC 都行。

👉 [了解 BGP Transit 方案](https://store.f4.network/index.php/order/main/packages/iptransit/a/NjAz)

---

## 这家适合谁？

说实话，F4 Networks 不是那种"买来就跑 WordPress"的傻瓜主机。他们的用户画像很清晰：

- **BGP 爱好者 / 网络极客**：想自己跑 BGP、折腾路由策略，F4 免费附带的 BGP Transit + IXP 端口是一个很低门槛的入口。
- **小型 ISP / WISP**：需要干净的上游，又不想掏大厂的价格。
- **需要 BYOIP 的技术用户**：自己持有 IP 段，想找个地方 announce，这里价格合适且支持。
- **东部或中部业务**：纽约 + 堪萨斯城的组合，对美国东海岸和中部的网络覆盖不错。

如果你只是需要一台普通 Linux 服务器跑个应用，$54/月的 m1.medium 也完全够用，10 Gbps 上 100TB 流量，怎么算都比很多大厂划算。

---

## 小结

F4 Networks 是那种"把预算花在硬件和网络上，而不是营销上"的小厂商。套餐直白，价格实在，BGP 功能是同价位少见的亮点，年付还能省下一个月的钱。

当然作为规模较小的独立托管商，稳定性和支持响应速度需要自行评估，建议先月付跑一段时间再决定是否长期绑定。

👉 [查看 F4 Networks 全部套餐并下单](https://store.f4.network/index.php/order/forms/a/NjAz)
