# 香港cn2大带宽vps：从1Gbps端口起步的三网优化机怎么挑，附全套餐价格与第三方实测带宽

搜“香港cn2大带宽vps”的人，大概率已经翻过一圈报价了。这个关键词下的香港套餐，端口普遍落在 3–50Mbps：tudcloud 给 30Mbps，小鸡云给 50Mbps，六六云给 30Mbps，再便宜一档还有标 2Mbps 的。换句话说，香港 CN2 语境里的“大带宽”，多数时候只是“比 5Mbps 大一点”。

真把香港节点端口做到 1Gbps 以上的商家不多。GoMami（圈内叫“狗妈”）是其中一个：香港 Turin 系列 2Gbps 起、最高 5Gbps，Pulse 系列 1Gbps 起、最高 3Gbps，三网回程统一走电信 CN2、联通 AS9929、移动 CMIN2。代价是价格——最便宜的香港套餐月付 $49 起。

## 选购速览

> 多数人会落在 **HKG.Pulse.Mini**（2 核 / 4GB / 60GB NVMe / 1TB 流量 / 1Gbps 端口，$59/月）或 **HKG.Turin.Mini**（2 核 / 4GB / 100GB NVMe / 1TB 流量 / 2Gbps 端口，$69/月）这两档。差 $10，换来多 40GB 硬盘、端口翻倍、CPU 从 EPYC 7763 换成 EPYC 9575F。要跑直播推流或大量上传的，先看完下面关于移动上行的部分再决定。

[👉 查看 HKG.Pulse.Mini 当前配置与价格](https://gomami.io/aff.php?aff=415&pid=4)

## 香港CN2大带宽VPS的“大带宽”到底指哪个单位

端口带宽和月流量是两个东西，宣传里经常混着说，混淆一次就可能买错。

端口带宽是瞬时上限，2Gbps 意味着网卡侧最多跑 2Gbps；月流量是计费额度，1TB 用完就得加钱或升档。2Gbps 端口配 1TB 流量，理论满速 70 分钟就把额度烧光。所以看到“大带宽”这个词，先确认商家说的是哪一个。

CN2 本身也值得说清楚。它是中国电信的下一代骨干网（AS4809），用来替代老旧的 163 网（AS4134），内部还分两档：CN2 GT 与普通流量共享容量，晚高峰会明显劣化，便宜的“CN2 VPS”多数是这一档；CN2 GIA 是独立高档，丢包接近零、延迟稳定，价格高一个量级。

GoMami 的官方口径比较克制：页面只写 CN2 / AS9929 / CMIN2 三网优化，产品线统一标 “China Mainland Optimized Pro”，没有写死“CN2 GIA”。第三方测评把它描述成三网各自顶级优化，那是测评者的说法。你在意线路等级的话，按“官方承诺三网各有专属优化路径”理解比较稳妥。

同样主打香港 CN2 的几家给的是什么量级，可以对照着看：

| 商家 / 套餐 | 配置 | 端口带宽 | 月流量 | 价格 |
| --- | --- | --- | --- | --- |
| tudcloud HK-1500GB | 3 核 / 6GB / 40GB SSD | 30Mbps | 1.5TB | $19.99/月 |
| 小鸡云 香港CN2大带宽 A 型 | 2 核 / 2GB / 30GB SSD | 50Mbps | 100GB | ¥29/月起 |
| 六六云 HK-CMI-1H1G-30M | 1 核 / 1GB / 20GB SSD | 30Mbps | 双向 500GB | ¥45/月 |
| Jtti 香港 CN2 | 1 核 / 2GB / 50GB SSD | 2Mbps | 不限量 | $48/年 |

这张表只用来确认端口量级。几家页面的采集时间并不一致（Jtti 那页标注 2026-05，其余页面未标日期），价格和配置随时会变，实际以各商家页面公示为准。三十兆、五十兆在这里已经算“大”的了——这也是 GoMami 那 1–5Gbps 显得突兀的原因：它卖的不是同一个量级的东西。

## GoMami 全部套餐与价格

香港是本文的主场，先列全。价格以 2026 年 8 月的公开标价快照为准；官网首页部分位置仍显示较早的标价（例如 Pulse.Mini 仍标 $39、40GB 硬盘的旧配置），下单前以结账页实际金额为准。

### 香港 Turin（AMD EPYC 9575F，最高约 5GHz）

| 套餐 | 配置 | 流量 / 端口 | 月付价（USD） | 购买 |
| --- | --- | --- | --- | --- |
| HKG.Turin.Mini | 2 核 / 4GB / 100GB NVMe | 1TB / 2Gbps | $69 | [ 选购](https://gomami.io/aff.php?aff=415&pid=14) |
| HKG.Turin.Air | 4 核 / 8GB / 140GB NVMe | 2TB / 2Gbps | $129 | [ 选购](https://bit.ly/Gomami) |
| HKG.Turin.Pro | 6 核 / 16GB / 180GB NVMe | 5TB / 5Gbps | $299 | [ 选购](https://bit.ly/Gomami) |
| HKG.Turin.Ultra | 12 核 / 32GB / 220GB NVMe | 10TB / 5Gbps | $599 | [ 选购](https://bit.ly/Gomami) |

Pro 与 Ultra 在购物车里标了 Windows-ready。

### 香港 Pulse（AMD EPYC 7763，最高 3.5GHz）

| 套餐 | 配置 | 流量 / 端口 | 月付价（USD） | 购买 |
| --- | --- | --- | --- | --- |
| HKG.Pulse.Nano | 2 核 / 2GB / 40GB NVMe | 500GB / 1Gbps | $49 | [ 选购](https://bit.ly/Gomami) |
| HKG.Pulse.Mini | 2 核 / 4GB / 60GB NVMe | 1TB / 1Gbps | $59 | [ 选购](https://gomami.io/aff.php?aff=415&pid=4) |
| HKG.Pulse.Air | 4 核 / 8GB / 80GB NVMe | 2TB / 1Gbps | $119 | [ 选购](https://bit.ly/Gomami) |
| HKG.Pulse.Pro | 8 核 / 16GB / 100GB NVMe | 5TB / 3Gbps | $269 | [ 选购](https://bit.ly/Gomami) |
| HKG.Pulse.Ultra | 12 核 / 32GB / 300GB NVMe | 10TB / 3Gbps | $499 | [ 选购](https://bit.ly/Gomami) |

### 香港 Ryzen 9 9950X 系列（官网首页单列，未标系列名）

| 套餐 | 配置 | 流量 / 端口 | 月付价（USD） | 购买 |
| --- | --- | --- | --- | --- |
| Mini | 2 核 / 4GB / 40GB NVMe | 1TB / 2Gbps | $59 | [ 选购](https://bit.ly/Gomami) |
| Air | 4 核 / 8GB / 60GB NVMe | 2TB / 2Gbps | $99 | [ 选购](https://bit.ly/Gomami) |
| Pro | 6 核 / 16GB / 80GB NVMe | 5TB / 5Gbps | $199 | [ 选购](https://bit.ly/Gomami) |

这条线用的是 AMD Ryzen 9 9950X，最高加速 5.7GHz，单核爆发力比 EPYC 更高；但同价位硬盘容量小于 Pulse 和 Turin，第三方实测里它的磁盘 IO 也被限制过（同样 10GB 测试文件的 dd 写入约 846 MB/s，明显低于 7763 版本的 2.3 GB/s）。跑游戏服、编译、单线程 API 可以看看，跑重度 IO 的应用不太合适。

### 香港 Forge（独立服务器，TYAN B8033 平台，EPYC 7663 56 核 112 线程）

| 套餐 | 配置 | 流量 / 端口 | 月付价（USD） | 购买 |
| --- | --- | --- | --- | --- |
| HKG.Forge.Mini | 128GB 内存 / 960GB NVMe | 10TB / 2Gbps | $599 | [ 选购](https://bit.ly/Gomami) |
| HKG.Forge.Air | 256GB 内存 / 4TB NVMe | 20TB / 2Gbps | $899 | [ 选购](https://bit.ly/Gomami) |

Forge 超流量按 $0.06/GB 计，附加 IP $10 一个、每台最多 4 个，付款后即时开通。

### 日本 / 新加坡 / 洛杉矶（同一套三网优化线路）

| 节点·套餐 | 配置 | 流量 / 端口 | 月付价（USD） | 购买 |
| --- | --- | --- | --- | --- |
| JPN.Pulse.Nano | 2 核 / 2GB / 40GB NVMe | 500GB / 1Gbps | $29 | [ 选购](https://bit.ly/Gomami) |
| JPN.Pulse.Mini | 2 核 / 4GB / 60GB NVMe | 1TB / 1.5Gbps | $49 | [ 选购](https://bit.ly/Gomami) |
| JPN.Pulse.Air | 4 核 / 8GB / 80GB NVMe | 2TB / 1Gbps | $89 | [ 选购](https://bit.ly/Gomami) |
| JPN.Pulse.Pro | 8 核 / 16GB / 100GB NVMe | 5TB / 3Gbps | $169 | [ 选购](https://bit.ly/Gomami) |
| JPN.Pulse.Ultra | 12 核 / 32GB / 300GB NVMe | 10TB / 3Gbps | $338 | [ 选购](https://bit.ly/Gomami) |
| SIN.Pulse.Nano | 2 核 / 2GB / 40GB NVMe | 500GB / 1Gbps | $29 | [ 选购](https://bit.ly/Gomami) |
| SIN.Pulse.Mini | 2 核 / 4GB / 60GB NVMe | 1TB / 1Gbps | $49 | [ 选购](https://bit.ly/Gomami) |
| SIN.Pulse.Air | 4 核 / 8GB / 80GB NVMe | 2TB / 1Gbps | $89 | [ 选购](https://bit.ly/Gomami) |
| SIN.Pulse.Pro | 8 核 / 16GB / 100GB NVMe | 5TB / 3Gbps | $169 | [ 选购](https://bit.ly/Gomami) |
| SIN.Pulse.Ultra | 12 核 / 32GB / 300GB NVMe | 10TB / 3Gbps | $338 | [ 选购](https://bit.ly/Gomami) |
| LAX.Pulse.Nano | 2 核 / 2GB / 40GB NVMe | 1TB / 1Gbps | $29 | [ 选购](https://bit.ly/Gomami) |
| LAX.Pulse.Mini | 2 核 / 4GB / 60GB NVMe | 2TB / 1Gbps | $59 | [ 选购](https://bit.ly/Gomami) |
| LAX.Pulse.Air | 4 核 / 8GB / 80GB NVMe | 4TB / 2Gbps | $129 | [ 选购](https://bit.ly/Gomami) |
| LAX.Pulse.Pro | 6 核 / 16GB / 100GB NVMe | 8TB / 3Gbps | $259 | [ 选购](https://bit.ly/Gomami) |
| LAX.Pulse.Ultra | 12 核 / 32GB / 300GB NVMe | 15TB / 5Gbps | $599 | [ 选购](https://bit.ly/Gomami) |
| LAX.Pulse.Titan | 12 核 / 32GB / 600GB NVMe | 30TB / 10Gbps | $999 | [ 选购](https://bit.ly/Gomami) |

按标价粗算每 TB 流量的成本：香港 HKG.Pulse.Ultra 约 $49.9/TB 最划算，HKG.Pulse.Pro 约 $53.8/TB，HKG.Pulse.Mini $59/TB，Turin.Mini $69/TB。洛杉矶 Titan 最低，$999 除 30TB 约 $33.3/TB。只追求吞吐量、不在意节点位置的话，美西那台的单位成本明显更低。

## 1–5Gbps 端口在实际线路里能跑出多少

单线程实测上限比标称端口低不少，瓶颈通常在你本地。2025 年底的一份第三方测评里，深圳电信 500Mbps 本地拉 HKG.Turin.Mini，单线程跑到 475Mbps（本地已满）；济南联通 500Mbps 本地跑出 545–572Mbps；另有一条移动线路下行跑到 933Mbps。

真正值得注意的是移动方向的上行。同一份测评里，广东移动 1Gbps 本地对香港节点上传只有约 37.5Mbps，下行 284Mbps。测评者的结论是香港和日本节点对移动上行存在 QoS，下行正常。这意味着：

- 下载、看视频、拉资源：三个地区都很猛，标称带宽基本吃满
- 直播推流、大文件上传、备份回源：移动宽带用户会被上行卡住，换套餐也解决不了

运营商差异也不小。测评结论是电信用户香港 ≈ 日本 > 新加坡；联通用户香港 > 日本 > 新加坡（联通到新加坡上行断流较明显）；移动用户反而是新加坡 > 日本 ≈ 香港。挑节点按自己主要用户的运营商来，比按“哪个机房新”靠谱。

另外 5201 端口的 iperf3 被屏蔽，自己测速记得换端口，不然会误判成线路不通。

## 谁适合买，谁买了会后悔

适合的：面向中国大陆用户的生产型站点、跨境电商、需要低延迟的游戏服务器或实时通信、把香港当落地节点做流媒体直出的用户。 Turin.Mini 的第三方实测数据是 2 核环境下 Geekbench 5 单核 2259 / 多核 4262，SysBench 单核 6173，fio 1M 块读写 8.03 GB/s——这些数字放在香港 VPS 里是什么水平，你自己对着看比听结论靠谱。

会后悔的：预算只有每月几美元的用户。GoMami 最便宜的套餐是日本、新加坡、洛杉矶三地的 Nano，均为 $29/月；香港起步 $49/月，和其他家 ¥29 起的香港 CN2 完全不在一个价格带。只是搭个博客、跑个轻量代理，它的性能和线路都是浪费，预算有限的个人用户去看别家更合适。

还有一个场景要注意：预算敏感又要大流量下载。香港 Pulse.Ultra 是 $499 给 10TB / 3Gbps；洛杉矶 Pulse.Ultra 是 $599 给 15TB / 5Gbps，多花 $100 换 5TB 流量和更高一档端口。纯按每 TB 成本算，后者更划算。

## 计费与政策里几个容易踩的点

流量是单向计费，只算 outbound，inbound 不计。不少同行标的是“双向 500GB”这类口径，比价时要换算过再比。

流量用完可以单独买流量包：100GB $6、500GB $30、1TB $60、2TB $120、5TB $300、10TB $600、20TB $1,200。流量包只对当前计费周期有效，不滚存。

这里有个算账上的细节。HKG.Turin.Mini 是 $69 含 1TB，加 1TB 流量包 $60，合计 $129；而 HKG.Turin.Air 本身就是 $129，含 2TB，还多 2 核、多 4GB 内存、多 40GB 硬盘。两者花的钱一模一样，升档等于硬件白送。除非你完全不想迁移数据，否则流量吃紧时优先升档。

[👉 对比 Turin.Air 与 Mini 的配置差价](https://bit.ly/Gomami)

退款政策是 24 小时内无风险取消、全额退款，但只限首次购买。续费订单不退，因 DDoS 被 blackhole 的 IP 也不在退款范围内。到账时间支付宝 1–3 个工作日、信用卡 5–10 个工作日、加密货币 1–3 个工作日。这条政策对“先买一个月实测线路再决定要不要年付”的用法很关键：月付 $59 试一台 HKG.Pulse.Mini，24 小时内跑完自己的 mtr 和 iperf3，不合适就退。

到期处理比较硬：到期日当天立即暂停，没有宽限期，逾期 5 天终止，数据可能无法恢复。续费账单会提前生成并邮件通知，也可以预充值余额走自动续费。

年付通常比月付省 15%–20%，具体折扣按产品线不同。官网没有公开各套餐的年付标价，只有在结账时切换计费周期才看得到实际数字，所以任何“某套餐年付价 $XXX”的说法都不该当成官方价格。

DDoS 防护这块，官网首页写的是最高 600Gbps 清洗能力，官方文档的表述是默认提供 best-effort 防护、600Gbps 为可选高级清洗。两处口径不同，别理解成每台机器默认带 600G 防护。

## 下单到开通的流程

付款后系统自动部署，通常 1–5 分钟完成，IP 和登录凭据发到邮箱。支持信用卡（Stripe）、支付宝（Stripe Alipay）和加密货币。

系统模板有 Ubuntu 22.04/24.04、Debian 11/12、CentOS Stream 9、AlmaLinux 8/9、Windows Server 2019/2022。需要 RouterOS 这类非常规系统时走自定义 ISO：挂载镜像、把启动顺序改成 CD-ROM、手动重启、通过 VNC 完成安装，装完必须卸载 ISO 并把启动顺序改回硬盘，否则下次重启又会进安装界面。从 ISO 装系统会覆盖硬盘数据，动手前先确认没别的东西在上面。

控制面板能看到 CPU、内存、网络流量的实时曲线，也支持 API Token 程序化管理和 2FA。

[👉 直接开通一台香港 Turin.Mini 做线路实测](https://gomami.io/aff.php?aff=415&pid=14)

## 几个常被问到的问题

**香港 CN2 VPS 真能跑到 1Gbps 吗？** 端口上限和单线程速度是两件事。标称 2Gbps 表示网卡侧上限，单线程实测受你本地带宽和运营商策略限制，电信、联通方向单线程稳定 500Mbps 左右是常见结果，多线程叠加才接近端口上限。移动方向上行为已知短板。

**CN2 GT 和 CN2 GIA 差在哪？** GT 与普通流量共享容量，晚高峰会劣化；GIA 是独立高档，丢包和延迟更稳，价格也高得多。GoMami 官方页面只写 CN2，没有标注 GT 还是 GIA，本文不替它升级这个说法。

**流量超了会停机吗？** 可以先买流量包补，或者直接升档。买之前算一下升档差价和流量包价格哪个更划算，多数情况下升档更值。

**能退款吗？** 新购 24 小时内可以全额退，仅限首次购买；超过 24 小时、续费订单、已使用的账户余额都不退。

**支持 Windows 吗？** Turin 的 Pro 和 Ultra 在购物车里标了 Windows-ready，系统模板包含 Server 2019/2022。其他档位的 Windows 支持情况官网没有明确说明，授权费用也没有公开，需要的话开工单确认。

## 按你的情况该怎么选

只想要一台香港机器跑站点、预算卡在 $50–60：HKG.Pulse.Mini，$59/月，2 核 4GB 60GB，1Gbps 端口配 1TB 流量，够中小站点和 API 服务用。

愿意多出 $10 换更好的单核和翻倍端口：HKG.Turin.Mini，$69/月，100GB 硬盘、2Gbps 端口、EPYC 9575F。做游戏服务器、实时接口、数据库这类吃单线程的业务，这 $10 花得值。

要多开虚拟机、跑 Windows、或者业务量上来了：HKG.Turin.Pro 的 6 核 16GB / 5TB / 5Gbps 是香港这边端口和流量的平衡点，$299/月。

要的是裸金属级别的独享资源：HKG.Forge.Mini，56 核 128GB，$599/月。它和同价的 Turin.Ultra 是两种完全不同的东西——后者是虚拟机但主频更高，前者是整台机器归你。

预算真的只有二三十美元：日本、新加坡、洛杉矶的 Nano 都是 $29/月，同价同配置，按你要覆盖的地区挑就行，香港这个价位没有对应产品。

不管选哪档，先月付、24 小时内跑完自己的实测再考虑长周期。年付折扣的具体数字在结账页切换周期时才看得到，任何第三方给出的年付价都只是估算。

[👉 按预算挑一台三网优化节点开通](https://bit.ly/Gomami)
