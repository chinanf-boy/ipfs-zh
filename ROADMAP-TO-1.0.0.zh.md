
# IPFS 1.0.0的路线图

## 目录

-   [描述](#description)
-   [里程碑](#milestones)

## 描述

为了使IPFS达到成熟状态,从Alpha到Beta,再到v1.0.0,项目将需要: 

-   因其规格100%完整. 这包括IPFS,libp2p,多格式和IPLD规范. 
-   符合性测试规范. 
-   golang和JavaScript实现是100%完整且符合规范. 
-   IPFS的第三方实现,可与go和JavaScript版本完全互操作. 
-   发布计划和周期,包括支持更长时间内特定密钥发布的策略 (即LTS版本与稳定版本) 

## 里程碑

在这里,您可以找到IPFS项目中达到1.0.0版本的各种挑战和里程碑的完整列表. 它们目前没有以任何方式排序,只是分组. 

### 可持续性和治理

这些是为IPFS创建积极,可持续,包容性和参与性治理模式的一些里程碑. 

-   [x] 组织IPFS所有人. 
-   [ ] 由指导工作组领导IPFS. 
-   [ ] 定义几个专注于项目不同部分的工作组 (例如社区参与,文档和教育,Web浏览器中的IPFS) . 
-   [ ] 定义发布计划和长期支持计划. 

### IPFS用例

这些是用于推动开发的一些用例里程碑. 

-   [x] 支持文件分发
    -   [x] 支持个人文件存储,备份和分发
    -   [x] 支持基本的p2p文件分发
    -   [x] 支持快速局域网文件分发
-   [x] 支持文件,网站,数据的不可变永久链接
-   [x] 支持文件,网站,数据的可变链接
-   [x] 支持网站和Web应用程序
    -   [x] 支持静态Web应用程序
    -   [x] 支持基于API的Web应用程序
    -   [x] 完全基于IPFS支持完全动态的网站 (例如聊天) 
-   [x] 支持协作播种/固定
    -   [x] ipfs ref pinning的基本支持
    -   [ ] 云ipfs前端服务 (多维数据集) 
    -   [ ] ipfs节点集群 (RAID / RAIN) 
    -   [ ] 拜占庭集群 (BA) 
-   [x] 支持浏览器
    -   [x] 选项卡内的js-ipfs-api客户端
    -   [x] 选项卡内的js-ipfs完整节点
    -   [x] 浏览器扩展网关重定向
    -   [x] 浏览器扩展完整节点
    -   [ ] 在浏览器中使用本机
-   [x] 支持版本控制和归档
    -   [x] 档案档案
    -   [x] 数据和数据库的存档
    -   [ ] 基于提交的版本控制
-   [x] 通过API支持其他工具或应用程序
    -   [x] 支持命令行API使用
    -   [x] 支持HTTP API使用
    -   [ ] 支持unix套接字RPC API用法
    -   [x] 支持嵌入式程序化API使用
    -   [x] 支持HTTP网关

### 绩效里程碑

这些是一些基本的性能里程碑. 

-   [x] 兆字节/慢
    -   [x] 足够小的文件 -  MB
    -   [x] 足够好的静态网站 -  MB
    -   [x] 足以分发webapp代码/资产 -  MB
    -   [x] 足够好的图像 -  MB
-   [x] 千兆字节
    -   [x] 足够好的个人文件 -  GB
    -   [x] 足以在网络上传输视频 -  GB
    -   [x] 足够小的科学数据集 -  GB
    -   [x] 足以分发webapp用户数据--GB
-   [ ] 兆兆字节
    -   [x] 足够好用于图像采集 -  TB
    -   [x] 适合小型视频收藏 -  TB
    -   [ ] 足够适合中等科学数据集 - 结核病
    -   [x] 足够好作为包经理 (gx)  -  TB
    -   [x] 作为包管理器备份 (npm-on-ipfs) 足够好 -  TB
    -   [ ] 作为包管理器更换 (npm-on-ipfs) 足够好 -  TB
    -   [x] 足以分发小型数据库 -  TB
    -   [ ] 足够大 (单) 档案 -  TB
-   [ ] 拍字节
    -   [ ] 足够适合大型视频收藏 -  PB
    -   [ ] 足够用于大型科学数据集 -  PB
    -   [ ] 足够好的备份档案 -  TB / PB
    -   [ ] 足以分发大型数据库 -  PB
-   [ ] 艾字节
    -   [ ] 足够好用于大规模档案 -  EB
    -   [ ] 足够好的整个网络 -  EB
    -   [ ] 对于排名前10的网站足够好 -  EB

### 开发人员库

这些是必须存在的一些库,以使开发人员的生活变得轻松. 在IPFS上制作完全动态的应用程序应该与传统系统一样简单或容易,这一点至关重要. 

-   [x] 文件导入器用于基本文件
-   [x] 自定义文件导入器工具
-   [x] ipfs节点api绑定
    -   [x] Go中的ipfs api绑定
    -   [x] JS中的ipfs api绑定
    -   [x] Java中的ipfs api绑定
    -   [x] Python中的ipfs api绑定
    -   [x] PHP中的ipfs api绑定
    -   [x] Ruby中的ipfs api绑定
    -   [ ] Scala中的ipfs api绑定
    -   [ ] Rust中的ipfs api绑定
    -   [ ] Haskell中的ipfs api绑定
    -   [x] C / C ++中的ipfs api绑定
    -   [ ] Erlang中的ipfs api绑定
-   [x] 完整的ipfs节点实现
    -   [x] go-ipfs  -  Go中的实现
    -   [x] js-ipfs  -  JS中的实现
-   [x] cli工具的开发人员库
-   [ ] 桌面应用程序的开发人员库
-   [x] 用于webapps的开发人员库
    -   [x] js-ipfs-api  -  js api绑定
-   [ ] 移动应用程序的开发人员库
    -   [ ] 适用于iOS的开发人员库
    -   [ ] 适用于Android的开发人员库
-   [x] node.js应用程序的开发人员库
    -   [x] go-ipfs-dep  - 安装go-ipfs的模块
    -   [x] ipfsd-ctl  - 控制ipfs守护进程的模块
    -   [x] js-ipfs-api  -  js api绑定
-   [ ] 用于动态webapps的开发人员库 (正在进行中) 
    -   [x] ipfs-log (CRDT) 
    -   [ ] 其他"IPFS上的CRDT"库
    -   [x] orbit-db  - 键值存储和事件日志
-   [ ] 用于加密功能的开发人员库
    -   [ ] 典型的ipfs共享模型
-   [ ] 社交网络的开发人员库
    -   [ ] POST数据结构
    -   [ ] 分散的身份

### 安全里程碑

-   [ ] 网络安全
    -   [x] 可升级的传输加密 (多流) 
    -   [x] 传输加密: secio (ECDHE) 
    -   [ ] 传输加密: TLS 1.3 (主流加密) 
    -   [ ] 传输加密: CurveCP或MinimaLT (djb加密) 
-   [ ] 内容安全
    -   [x] 内容安全: IPLD哈希链接 (经过身份验证的内容) 
    -   [ ] 内容安全: Keychain签名对象
    -   [ ] 内容安全: 本机内容加密
    -   [ ] 内容安全: 本机加密功能
    -   [ ] 内容安全: 审计
-   [ ] 匿名
    -   [ ] 匿名运输: 支持
    -   [ ] 匿名传输: i2p支持
    -   [ ] 船舶匿名聚焦分布 (tor,i2p,没有泄漏信息) 
    -   [ ] 对等和内容路由匿名
    -   [ ] 匿名: 审计
-   [ ] Anticensorship
    -   [x] 反审查: 分散,对等的内容分发
    -   [x] 防御: 基于访问的重新分配
    -   [ ] 反审: 激励分配
    -   [ ] 反审: PKI分发
    -   [ ] 防御: 对强大的sybil路由攻击的恢复能力
    -   [ ] 防御: HTTP TLS传输仿真
-   [ ] 审计
    -   [ ] 审计: 完整协议模糊测试
    -   [ ] 审计: 使用最先进的漏洞测试套件进行测试
    -   [ ] 审计: p2p可扩展性研究员审计
    -   [ ] 审计: 全面协议的3次独立专业安全审计
    -   [ ] 审计: 3x独立的专业安全审计实施

### 网络可扩展性

IPFS协议的可扩展性取决于精心设计的算法和模型,仔细优化我们的实现,并仔细关注协议的安全属性. 虽然可以实现,但是为自组织对等协议实现高可扩展性是很难的. 我们测量数量级的可扩展性,因为更大的阈值需要重新访问我们代码库的各个部分. 

请记住,我们目前仍在实施协议的主要功能并实现完成. 我们还没有将注意力转向可扩展性,因此有很多低成本要优化,并且可能会产生许多可扩展性错误. 最重要的部分是确保所有协议都可以扩展到数十亿个节点,并且它们不会进行集中化假设. 我们选择的所有协议都没有做出小规模的假设,并且意味着可以很好地扩展 (通常`log(n)`) . 

我们的可扩展性观察分为模拟,真实网络测试和生产网络. 

-   [x] 模拟
    -   [x] 可扩展到1,000个节点
    -   [x] 可扩展到10,000个节点
    -   [x] 可扩展到100,000个节点
    -   [ ] 可扩展到1,000,000个节点
    -   [ ] 可扩展到1,000,000,000个节点
-   [x] 真正的网络测试
    -   [x] 可扩展到1,000个节点
    -   [x] 可扩展到10,000个节点
    -   [ ] 可扩展到100,000个节点
    -   [ ] 可扩展到1,000,000个节点
    -   [ ] 可扩展到1,000,000,000个节点
-   [x] 生产网络
    -   [x] 可扩展到1,000个节点
    -   [x] 可扩展到10,000个节点
    -   [ ] 可扩展到100,000个节点
    -   [ ] 可扩展到1,000,000个节点
    -   [ ] 可扩展到1,000,000,000个节点

### 波兰水平

达到的润色级别定义了对工具,API,文档等所有角落进行了多少努力. 在早期,事情会更加艰难,因为我们需要专注于最终抛光的实施速度. 随着我们完成实施,我们将注意力转向可扩展性,稳定性和安全性. 之后,我们专注于最终用户润色. 

-   [x] 波兰水平: 阿尔法 - 个人创新者
-   [x] 波兰语水平: alpha  - 早期采用者的生产
-   [ ] 波兰级别: 测试版 - 小型组织的生产 (进行中) 
-   [ ] 波兰级别: 测试版 - 大型组织的生产
-   [ ] 波兰水平: 1.0  - 所有人的生产

### Multiformats

多格式是一组自我描述的协议/格式,用于面向未来或"可升级的系统" (不会产生任何可能随时间推移的愚蠢假设的系统) . 

-   [x] multiaddr: 协议设计
    -   [x] multiaddr: Go中的impl
    -   [x] multiaddr: JS中的impl
    -   [x] multiaddr: Java中的impl
    -   [x] multiaddr: Haskell中的impl
    -   [x] multiaddr: Python中的impl
    -   [x] multiaddr: Rust中的impl
-   [x] multihash: 协议规范
    -   [x] multihash: Go中的impl
    -   [x] multihash: JS中的impl
    -   [x] multihash: Scala中的impl
    -   [x] multihash: Java中的impl
    -   [x] multihash: Clojure中的impl
    -   [x] multihash: 在Rust中impl
    -   [x] multihash: 在Haskell中的impl
    -   [x] multihash: Python中的impl
    -   [x] multihash: 在Elixir中的impl
    -   [x] multihash: Swift中的impl
    -   [x] multihash: Ruby中的impl
-   [x] multicodec: 协议规范
    -   [x] multicodec: Go中的impl
    -   [x] multicodec: JS中的impl
-   [x] 多流: 协议规范
    -   [x] 多流: Go中的impl
    -   [x] multistream: JS中的impl
-   [x] multibase / baseN: 协议规范
    -   [x] multibase / baseN: Go中的impl
    -   [x] multibase / baseN: JS中的impl

### libp2p协议

libp2p协议是从IPFS中分离出来的模块化p2p协议库的协议栈. 这些形成了p2p优先的网络堆栈,没有假设,自我描述和模块化接口. 更多<https://github.com/ipfs/specs/tree/master/libp2p>

-   [x] libp2p架构
    -   [x] go中的libp2p impl
    -   [x] JS中的libp2p impl
-   [x] 识别协议接口
    -   [x] 识别: Go中的impl
    -   [x] 识别: JS中的impl
-   [x] 传输协议接口
    -   [x] 传输协议: Go中的TCP
    -   [x] 传输协议: JS节点中的TCP
    -   [x] 传输协议: Go中的UTP
    -   [x] 传输协议: JS节点中的UTP
    -   [x] 传输协议: Go中的UDT
    -   [ ] 传输协议: JS节点中的UDT
    -   [x] 传输协议: Go中的WebSockets
    -   [x] 传输协议: JS节点中的WebSockets
    -   [x] 传输协议: JS浏览器中的WebSockets
    -   [ ] 传输协议: Go中的WebRTC
    -   [x] 传输协议: JS节点中的WebRTC
    -   [x] 传输协议: JS浏览器中的WebRTC
    -   [ ] 传输协议: Go中的SCTP
    -   [ ] 传输协议: JS节点中的SCTP
    -   [ ] 传输协议: 转到Go
    -   [ ] 传输协议: 在JS节点中
    -   [ ] 传输协议: Go中的i2p
    -   [ ] 传输协议: JS节点中的i2p
    -   [ ] 传输协议: Go中的cjdns
    -   [ ] 传输协议: JS节点中的cjdns
    -   [ ] 传输协议: Go中的蓝牙LE
    -   [ ] 传输协议: JS节点中的蓝牙LE
    -   [ ] 传输协议: Go中的音频TP
    -   [ ] 传输协议: JS节点中的音频TP
    -   [ ] 传输协议: Go中的Zerotier
    -   [ ] 传输协议: JS节点中的Zerotier
    -   [ ] 传输协议: Go中的QUIC
    -   [ ] 传输协议: JS节点中的QUIC
-   [x] Stream Muxer: 接口
    -   [x] Stream Muxer: Go中的基准测试
    -   [x] Stream Muxer: JS中的基准测试
    -   [x] Stream Muxer: Go中的muxado
    -   [x] Stream Muxer: Go中的spdystream
    -   [x] Stream Muxer: Go中的Multiplex
    -   [x] Stream Muxer: JS中的Multiplex
    -   [x] Stream Muxer: JS中的spdy
    -   [ ] Stream Muxer: Go中的http2
    -   [ ] Stream Muxer: JS中的http2
    -   [ ] Stream Muxer: Go中的QUIC
    -   [ ] Stream Muxer: JS中的QUIC
-   [x] 交换机: 接口
    -   [x] Go中的拨号器堆栈
    -   [x] JS中的拨号器堆栈
    -   [x] 在Go中切换实现
    -   [x] 在JS中切换实现
-   [x] NAT Traversal: 接口
    -   [x] Go中的nat-pmp实现
    -   [ ] JS中的nat-pmp实现
    -   [x] Go中的upnp实现
    -   [ ] JS中的upnp实现
    -   [x] Go中的ext addr发现
    -   [ ] JS中的ext addr发现
    -   [ ] Go中的STUN式实现
    -   [ ] JS中类似STUN的实现
    -   [x] Go中的线路交换中继实现
    -   [ ] JS中的线路交换中继实现
    -   [ ] Go中的pkt-switch中继实现
    -   [ ] JS中的pkt-switch relay实现
-   [x] 同行发现: 接口
    -   [x] 同行发现: Go中的mDNS
    -   [x] 同行发现: JS中的mDNS
    -   [x] Peer Discovery: JS中的bootstrap列表
    -   [x] Peer Discovery: Go中的bootstrap列表
    -   [x] 同行发现: JS中的DHT查询
    -   [x] 同行发现: Go中的DHT查询
    -   [ ] 同行发现: JS中的PEX
    -   [ ] 同行发现: Go中的PEX
    -   [ ] 同行发现: JS中的DNS
    -   [ ] 同行发现: Go中的DNS
-   [x] 内容路由: 协议接口
    -   [x] 内容路由: Go中的Kademlia DHT impl
    -   [x] 内容路由: JS中的Kademlia DHT impl
    -   [ ] 内容路由: Go中的pub / sub impl
    -   [ ] 内容路由: JS中的pub / sub impl
    -   [ ] 内容路由: Go中的PHT
    -   [ ] 内容路由: JS中的PHT
-   [x] 对等路由: 协议接口
    -   [x] 对等路由: Go中的Kademlia DHT impl
    -   [x] 对等路由: JS中的Kademlia DHT impl
    -   [ ] 对等路由: Go中的pub / sub impl
    -   [ ] 对等路由: JS中的pub / sub impl
    -   [ ] 对等路由: Go中的PHT
    -   [ ] 对等路由: JS中的PHT
-   [x] 交换: 协议接口
    -   [x] Exchange: Go中的HTTP
    -   [x] Exchange: JS中的HTTP
    -   [x] 交换: Go中的Bitswap
    -   [x] 交流: JS中的Bitswap
    -   [x] 交流: Go中的Bittorrent
    -   [x] Exchnage: JS中的Bittorrent
-   [ ] 共识: 协议接口
    -   [ ] 共识: Paxos
    -   [ ] 共识: 筏
    -   [ ] 共识: PBFT
    -   [ ] 共识: Nakamoto

### 比特交换

Bitswap是IPFS的交换协议. 它模拟数据市场. 

-   [x] Bitswap: 协议和架构设计
    -   [x] Bitswap: 协议规范
    -   [x] Bitswap: 决策引擎
    -   [x] Bitswap: 策略: 利他主义者
    -   [x] Bitswap: 策略: 后勤
    -   [x] Bitswap: 策略: 可编程
    -   [x] Bitswap: 支持密钥
    -   [x] Bitswap: 支持路径
    -   [ ] Bitswap: 支持选择器
    -   [ ] Bitswap: 其他txns的钩子
-   [x] Bitswap: Go中的impl
    -   [x] Bitswap: 测试模拟器
    -   [x] Bitswap: 基本交流
    -   [x] Bitswap: 带宽计费
    -   [x] Bitswap: 决策引擎
    -   [x] Bitswap: 策略: 利他主义者
    -   [ ] Bitswap: 策略: 后勤
    -   [ ] Bitswap: 策略: 可编程
    -   [x] Bitswap: 支持密钥
    -   [ ] Bitswap: 支持路径
    -   [ ] Bitswap: 支持选择器
    -   [ ] Bitswap: 其他txns的钩子
-   [x] Bitswap: JS中的impl
    -   [x] Bitswap: 测试模拟器
    -   [x] Bitswap: 基本交流
    -   [x] Bitswap: 带宽计费
    -   [x] Bitswap: 决策引擎
    -   [x] Bitswap: 策略: 利他主义者
    -   [ ] Bitswap: 策略: 后勤
    -   [x] Bitswap: 策略: 可编程
    -   [x] Bitswap: 支持密钥
    -   [ ] Bitswap: 支持路径
    -   [ ] Bitswap: 支持选择器
    -   [ ] Bitswap: 其他txns的钩子
-   [x] Bitswap: bssim网络模拟
    -   [x] Bitswap: bssim: 基本的进程内模拟
    -   [x] Bitswap: bssim: 基本的多进程仿真
    -   [ ] Bitswap: bssim: 基本的多机模拟
    -   [x] Bitswap: bssim: metrics集合
    -   [x] Bitswap: bssim: 报道
    -   [x] Bitswap: bssim: 可插拔策略
    -   [ ] Bitswap: bssim: 策略配置

### IPFS DHT

IPFS DHT (今天) 是基于Kademlia的DHT,实现了几种libp2p协议: 对等发现,对等路由,内容路由和一些NAT遍历协助. 

-   [x] IPFS DHT: 协议和架构设计
    -   [x] IPFS DHT: 协议规范/消息
    -   [x] IPFS DHT: kad查询
    -   [x] IPFS DHT: kbucketing
    -   [x] IPFS DHT: 抗冲击性
    -   [ ] IPFS DHT: 检查阻力
-   [x] IPFS DHT: Go中的impl
    -   [x] IPFS DHT: 消息
    -   [x] IPFS DHT: kad查询
    -   [x] IPFS DHT: kbucketing
    -   [x] IPFS DHT: 抗冲击性
    -   [ ] IPFS DHT: 检查阻力
-   [x] IPFS DHT: JS中的impl
    -   [x] IPFS DHT: 消息
    -   [x] IPFS DHT: kad查询
    -   [x] IPFS DHT: kbucketing
    -   [x] IPFS DHT: 抗冲击性
    -   [ ] IPFS DHT: 检查阻力
-   [x] IPFS DHT: dhtHell模拟
    -   [x] IPFS DHT: dhtHell可编程配置
    -   [x] IPFS DHT: dhtHell进程内测试
    -   [ ] IPFS DHT: dhtHell多进程测试
    -   [ ] IPFS DHT: dhtHell多机测试
    -   [x] IPFS DHT: dhtHell 1,000个节点
    -   [x] IPFS DHT: dhtHell 10,000个节点
    -   [ ] IPFS DHT: dhtHell 100,000个节点
    -   [ ] IPFS DHT: dhtHell 1,000,000个节点

### IPFS pub / sub

IPFS发布/订阅服务将为ipfs节点的子网提供快速传递和路由. 这对于动态应用程序至关重要. 发布/发布 (或多播) 将实现: 对等发现,对等路由,内容路由和一些NAT遍历协助. 它履行与IPFS DHT类似的角色,但具有截然不同的性能,安全性和可扩展性保证. IPFS Pub / Sub目前正在开发中. 

-   [ ] IPFS pub / sub: 协议和架构设计
    -   [ ] IPFS pub / sub: 协议规范/消息
    -   [ ] IPFS pub / sub: 记录规范
    -   [x] IPFS pub / sub: 单跳支持
    -   [ ] IPFS pub / sub: 多跳树形成
    -   [ ] IPFS pub / sub: churn resistance
    -   [ ] IPFS pub / sub: 审查阻力
    -   [ ] IPFS pub / sub: 主题/频道支持
    -   [ ] IPFS pub / sub: 分层主题/渠道支持
    -   [ ] IPFS pub / sub: 经过身份验证的子网
    -   [ ] IPFS pub / sub: 私有子网 (对称) 
    -   [ ] IPFS pub / sub: 私有子网 (PKI) 
-   [ ] IPFS pub / sub: Go中的impl
    -   [x] IPFS pub / sub: Go中的原型设计
-   [ ] IPFS pub / sub: JS中的impl
    -   [x] IPFS pub / sub: JS中的原型设计
-   [ ] IPFS pub / sub: pssim模拟
    -   [ ] IPFS pub / sub: pssim可编程配置
    -   [ ] IPFS pub / sub: pssim in-proc测试
    -   [ ] IPFS pub / sub: pssim多进程测试
    -   [ ] IPFS pub / sub: pssim多机测试
    -   [ ] IPFS pub / sub: pssim 1,000个节点
    -   [ ] IPFS pub / sub: pssim 10,000个节点
    -   [ ] IPFS pub / sub: pssim 100,000个节点
    -   [ ] IPFS pub / sub: pssim 1,000,000个节点

### IPLD

IPLD是IPFS数据的核心格式. 更多<https://github.com/ipfs/specs/tree/master/ipld>

-   [x] ipld v0 protobuf: spec
    -   [x] ipld v0 protobuf: impl in go
    -   [x] ipld v0 protobuf: imps in js
-   [x] ipld: spec
    -   [x] ipld: 链接
    -   [x] ipld: 路径
    -   [ ] ipld: 选择器
    -   [ ] ipld: 查询
    -   [x] ipld: v0 compat
    -   [x] ipld: cbor序列化
    -   [x] ipld: 链接和解析
    -   [x] ipld: 流媒体支持
-   [x] ipld: 进入Go
    -   [x] ipld: 链接
    -   [x] ipld: 路径
    -   [ ] ipld: 选择器
    -   [ ] ipld: 查询
    -   [x] ipld: v0 compat
    -   [x] ipld: cbor序列化
    -   [x] ipld: 链接和解析
    -   [x] ipld: 流媒体支持
-   [x] ipld: JS中的impl
    -   [x] ipld: 链接
    -   [x] ipld: 路径
    -   [ ] ipld: 选择器
    -   [ ] ipld: 查询
    -   [x] ipld: v0 compat
    -   [x] ipld: cbor序列化
    -   [x] ipld: 链接和解析
    -   [ ] ipld: 流媒体支持
-   [ ] ipld: 网站
    -   [ ] ipld: 网站: 首页
    -   [ ] ipld: 网站: 规范
    -   [ ] ipld: 网站: 关于
    -   [ ] ipld: 网站: 游乐场
        -   [ ] ipld: 网站: 游乐场规格
        -   [ ] ipld: website: playground impl

### IPLD数据结构和进口商

IPLD数据结构和导入程序是各种数据结构和程序,用于将来自其他本机表示的数据或文件转换为IPLD图和来自IPLD图. 可以将它们视为图形表示数据结构和转换编解码器. 

-   [x] unixfs for unix / posix文件
    -   [x] unixfs规范
        -   [x] unixfs文件
        -   [x] unixfs文件分片
        -   [x] unixfs文件trickledag
        -   [x] unixfs目录
        -   [ ] unixfs目录分片
        -   [x] unixfs元数据
    -   [x] unixfs impl in Go
        -   [x] unixfs文件
        -   [x] unixfs文件分片
        -   [x] unixfs文件trickledag
        -   [x] unixfs目录
        -   [x] unixfs目录分片
        -   [x] unixfs元数据
    -   [x] JS中的unixfs impl
        -   [x] unixfs文件
        -   [x] unixfs文件分片
        -   [x] unixfs文件trickledag
        -   [x] unixfs目录
        -   [x] unixfs目录分片
        -   [x] unixfs元数据
-   [x] 档案规范
    -   [x] 柏油
    -   [ ] 压缩
    -   [ ] rar
-   [ ] 钥匙扣规格
    -   [ ] 钥匙串: 钥匙
    -   [ ] 钥匙扣: sigs
    -   [ ] 钥匙串: 帽子
    -   [ ] 钥匙串: 证明

### IPFS回购

更多<https://github.com/ipfs/specs>和<https://github.com/ipfs/fs-repo-migrations>

-   [x] IPFS回购规范
    -   [x] Go中的IPFS repo impl
    -   [x] JS节点中的IPFS repo impl
    -   [x] JS浏览器中的IPFS repo impl
-   [x] IPFS fs-repo规范
    -   [x] IPFS fs-repo v0
        -   [x] IPFS fs-repo数据存储 (块和元数据) 
        -   [x] IPFS fs-repo配置文件
        -   [x] IPFS fs-repo锁定文件
        -   [x] IPFS fs-repo记录目录
    -   [x] IPFS fs-repo v1
        -   [x] IPFS fs-repo版本文件
        -   [x] IPFS fs-repo api文件
        -   [x] IPFS fs-repo块 (数据) 
        -   [x] IPFS fs-repo数据存储 (元数据) 
    -   [x] IPFS fs-repo v2
        -   [x] IPFS fs-repo ipld pinset
    -   [x] Go中的IPFS fs-repo impl
    -   [x] JS节点中的IPFS fs-repo impl
    -   [x] JS浏览器中的IPFS fs-repo impl
    -   [x] IPFS fs-repo-migrations
        -   [x] IPFS fs-repo-migrations 0-to-1
        -   [x] IPFS fs-repo-migrations 1-to-2
        -   [x] IPFS fs-repo-migrations 2到3

### IPFS协议和架构

-   [x] IPFS架构: 宏协议架构
-   [x] IPFS架构: 未来防御和自我描述 (multis) 
-   [x] IPFS架构: 网络
    -   [x] IPFS架构: 加密和经过身份验证的连接
    -   [x] IPFS架构: 对等和内容路由
    -   [x] IPFS架构: NAT遍历
    -   [x] IPFS架构: 线路和pkt交换中继
    -   [x] IPFS架构: 抽象和提取libp2p
    -   [x] IPFS架构: 基本专用网络 (对称加密) 
    -   [ ] IPFS架构: 高级专用网络 (PKI) 
-   [x] IPFS架构: merkle-linked图和IPLD
    -   [x] IPFS架构: fs和web的路径模型
    -   [x] IPFS体系结构: 用于图遍历的选择器
-   [x] IPFS架构: 寻址
    -   [x] IPFS架构: 内容寻址和解析
    -   [x] IPFS架构: 密钥寻址和解决方案
    -   [x] IPFS架构: 其他解析器寻址和解析
-   [x] IPFS架构: 节点数据同步模型
    -   [x] IPFS架构: ref pull resolution和retrieval
    -   [ ] IPFS架构: ref push
    -   [x] IPFS架构: ref pinning
    -   [ ] IPFS架构: 点对点RPC身份验证
-   [x] IPFS架构: 协议到程序的投影
    -   [x] IPFS架构: 程序模型
    -   [x] IPFS架构: 服务设计
    -   [x] IPFS架构: 工具设计
    -   [x] IPFS架构: 核心api设计
        -   [x] IPFS架构: cli api设计
        -   [x] IPFS架构: http api设计
        -   [ ] IPFS架构: RPC api设计
-   [x] IPFS架构: 程序的分发
-   [x] IPFS架构: webui设计
-   [x] IPFS架构: 应用程序设计
-   [ ] IPFS架构: 可编程策略挂钩
    -   [ ] IPFS架构: bitswap策略和交易
    -   [ ] IPFS架构: 数据广告和服务
    -   [ ] IPFS架构: 社交网络
    -   [x] IPFS架构: 阻止列表设计
        -   [ ] IPFS架构: 网关中的阻止列表支持
        -   [ ] IPFS架构: 网络中的阻止列表支持
        -   [ ] IPFS架构: 可扩展的阻止列表 (bloom) 
-   [ ] IPFS架构: 集群
    -   [ ] IPFS架构: 集群RAID / RAIN模式
    -   [ ] IPFS架构: 集群共识

### 去实施IPFS

go-ipfs工作是IPFS的Go实现. 它旨在作为命令行工具,作为后台服务,作为编程嵌入式节点,通过RPC API运行,并用作其他工具的一部分. go-ipfs是IPFS的参考实现. 它包括HTTP-to-IPFS网关实现. 更多<https://github.com/ipfs/go-ipfs>

-   [x] go-ipfs ipfs节点组件
    -   [x] go-ipfs多协议
    -   [x] go-ipfs组件: repo
    -   [x] go-ipfs组件: 网络 (libp2p) 
    -   [x] go-ipfs组件: bitswap
    -   [x] go-ipfs组件: dag / ipld
    -   [x] go-ipfs组件: 固定
    -   [x] go-ipfs组件: 块api
    -   [x] go-ipfs组件: 对象api
    -   [x] go-ipfs组件: 文件api
    -   [x] go-ipfs组件: 守护进程
    -   [x] go-ipfs组件: 数据导入
    -   [x] go-ipfs组件: 网关
    -   [x] go-ipfs组件: http api
-   [x] go-ipfs ipfs node api
    -   [x] go-ipfs core api impl
        -   [x] go-ipfs core api: 版本
        -   [x] go-ipfs core api: daemon
        -   [x] go-ipfs core api: id
        -   [x] go-ipfs core api: block
        -   [x] go-ipfs core api: object
        -   [x] go-ipfs core api: refs
        -   [x] go-ipfs core api: repo
        -   [x] go-ipfs core api: pin
        -   [x] go-ipfs core api: log
    -   [x] go-ipfs ext api impl
        -   [x] go-ipfs ext api: name (ipns) 
        -   [x] go-ipfs ext api: dns
        -   [x] go-ipfs ext api: tar
        -   [ ] go-ipfs ext api: tour
        -   [x] go-ipfs ext api: files
        -   [x] go-ipfs ext api: stat
        -   [x] go-ipfs ext api: mount
        -   [x] go-ipfs ext api: bootstrap
        -   [x] go-ipfs ext api: bitswap
    -   [x] go-ipfs tool api impl
        -   [x] go-ipfs tool api: init
        -   [x] go-ipfs tool api: config
        -   [x] go-ipfs tool api: update
        -   [x] go-ipfs tool api: 命令
    -   [x] go-ipfs net api impl
        -   [x] go-ipfs net api: ping
        -   [x] go-ipfs net api: dht
        -   [x] go-ipfs net api: swarm
        -   [ ] go-ipfs net api: 记录
-   [x] go-ipfs cli api impl
    -   [x] go-ipfs cli编解码器
-   [x] go-ipfs http api impl
    -   [x] go-ipfs http api: 流媒体
    -   [x] go-ipfs http api: multipart

### JFS实现IPFS

js-ipfs工作是IPFS的javascript实现. 它可以在node.js和今天的常规Web浏览器上运行. 它很接近,但尚未准备好. 更多<https://github.com/ipfs/js-ipfs>

-   [x] js-ipfs ipfs节点组件
    -   [x] js-ipfs多协议
    -   [x] js-ipfs组件: repo
    -   [x] js-ipfs组件: 网络 (libp2p) 
    -   [x] js-ipfs组件: bitswap
    -   [x] js-ipfs组件: dag / ipld
    -   [x] js-ipfs组件: 固定
    -   [x] js-ipfs组件: 块api
    -   [x] js-ipfs组件: 对象api
    -   [x] js-ipfs组件: 文件api
    -   [x] js-ipfs组件: 守护进程
    -   [x] js-ipfs组件: 数据导入
    -   [x] js-ipfs组件: http api
-   [ ] js-ipfs ipfs node api
    -   [x] js-ipfs core api impl
        -   [x] js-ipfs core api: 版本
        -   [x] js-ipfs core api: 守护进程
        -   [x] js-ipfs core api: id
        -   [x] js-ipfs core api: block
        -   [x] js-ipfs core api: object
        -   [ ] js-ipfs core api: refs
        -   [x] js-ipfs core api: repo
        -   [x] js-ipfs core api: pin
        -   [ ] js-ipfs core api: log
    -   [ ] js-ipfs ext api impl
        -   [ ] js-ipfs ext api: name (ipns) 
        -   [ ] js-ipfs ext api: dns
        -   [ ] js-ipfs ext api: tar
        -   [x] js-ipfs ext api: 文件
        -   [ ] js-ipfs ext api: stat
        -   [ ] js-ipfs ext api: mount
        -   [x] js-ipfs ext api: bootstrap
        -   [x] js-ipfs ext api: bitswap
    -   [x] js-ipfs工具api impl
        -   [x] js-ipfs工具api: init
        -   [x] js-ipfs tool api: config
        -   [ ] js-ipfs工具api: 更新
        -   [x] js-ipfs tool api: 命令
    -   [ ] js-ipfs net api impl
        -   [x] js-ipfs net api: ping
        -   [ ] js-ipfs net api: dht
        -   [x] js-ipfs net api: swarm
        -   [ ] js-ipfs net api: 记录
-   [x] js-ipfs cli api impl
-   [x] js-ipfs http api impl
    -   [x] js-ipfs http api: 流媒体
    -   [x] js-ipfs http api: multipart

### IPFS直接在浏览器上

作为Web协议,IPFS的最终目标是直接在浏览器中运行. 我们通过四步计划实现这一目标: 

-    (1) 以任何语言实现IPFS,并使用js-ipfs-api库将命令委托给IPFS API (例如,在localhost上运行的go-ipfs) . 这已经在今天运行,并且已经存在许多应用程序以这种方式在浏览器中利用IPFS.  (2) 在javascript中实现IPFS,并在浏览器选项卡中直接使用js-ipfs. 
-   这在今天正在进行中.  (3) 构建使用IPFS提供IPFS URI的浏览器扩展,并将ipfs暴露给浏览器选项卡. 
-   这可以使用go-ipfs (localhost上的API) 或理想情况下捆绑的js-ipfs来完成. 这在今天正在进行中. firefox扩展已经拥有400多名每日用户.  (4) 最后,向主要浏览器提交补丁,添加IPFS支持. 
-   我们已经完成了步骤 (1) . 

我们目前正在制定步骤 (2) 和 (3) . 

-   [x] 步骤 (4) 可能是2017年的努力. 浏览器选项卡中使用的IPFS API
    -   [x] go-ipfs实现
    -   [x] js-ipfs-api客户端库
    -   [x] 使用后台go-ipfs节点 (localhost或其他地方) 
-   [x] 在浏览器选项卡中运行的IPFS协议,在js中
    -   [x] js-libp2p实现
    -   [x] js-ipfs实现
    -   [x] libp2p.js浏览器库
    -   [x] ipfs.js浏览器库
-   [x] 使用浏览器扩展名运行的IPFS
    -   [x] go-ipfs实现
    -   [x] js-ipfs实现
    -   [x] firefox扩展
        -   [x] 使用后台go-ipfs节点
        -   [ ] 易于安装go-ipfs节点
        -   [x] 捆绑js-ipfs节点
        -   [x] 网址重写
        -   [x] 节点管理
        -   [x] api配置
        -   [ ] 简单的用户体验
        -   [ ] 在浏览器窗口中显示ipfs和p2p
    -   [x] 镀铬扩展
        -   [x] 使用后台go-ipfs节点
        -   [ ] 易于安装go-ipfs节点
        -   [x] 捆绑js-ipfs节点
        -   [x] 网址重写
        -   [ ] 节点管理
        -   [ ] api配置
        -   [ ] 简单的用户体验
        -   [x] 在浏览器窗口中显示ipfs和p2p
-   [ ] IPFS在浏览器中本机运行
    -   [x] go-ipfs实现 (用于chrome或firefox) 
        -   [ ] go-ipfs static lib (用于chrome或firefox) 
    -   [x] js-ipfs实现 (用于chrome或firefox) 
    -   [ ] rust-ipfs实现 (用于伺服) 
    -   [ ] 铬补丁添加IPFS支持
    -   [ ] firefox补丁添加IPFS支持
    -   [ ] 伺服补丁添加IPFS支持
    -   [ ] safari补丁添加IPFS支持

### IPFS节点管理控制台 (webui) 

我们有一个ipfs节点"管理控制台"GUI,作为分布式webapp (dapp) 提供. 这显示了有关ipfs节点的信息,并允许发出一些命令. webui完全通过IPFS本身托管和分发,在IPFS上演示动态Web应用程序. 更多<https://github.com/ipfs/webui>

-   [x] webui控制台架构
    -   [x] R / W特权API路由 (: 5001) 
        -   [x] 安全性: 起源和CORS
        -   [x] 安全性: 仅在本地暴露
        -   [ ] 安全性: 基于令牌的访问
    -   [x] 通过IPFS本身分发
    -   [x] 通过http-to-ipfs网关访问
-   [x] webui console v0
    -   [x] webapp设计
    -   [x] 基本节点信息
    -   [x] 同行地图 (3D地球) 
    -   [x] ipfs dag explorer
    -   [x] ipfs文件查看器
        -   [x] 列出所有文件
        -   [x] 添加文件 (+拖放) 
    -   [x] 尾日志 (json) 
    -   [x] 查看和编辑配置 (json) 
-   [x] webui console v1
    -   [x] webapp重新设计
    -   [x] 同行地图 (平面和3D) 
    -   [x] 新的dag探险家
    -   [x] 新文件资源管理器
        -   [x] 文件导航
        -   [x] 拖放支持
        -   [x] 文件预览

### HTTP到IPFS网关

为了简化IPFS的采用和部署,我们有HTTP-to-IPFS网关. 这意味着两个相关的事情:  (a) HTTP-to-IPFS网关服务器的实现 (当前是go-ipfs的一部分) ,以及 (b) 为社区运行的全局可访问服务Protocol Labs. 所有官方IPFS网站现在都直接在IPFS上自行托管. 

-   [x] HTTP网关实现 (在go-ipfs中) 
    -   [x] HTTP网关文件列表
    -   [x] 用于文件的HTTP网关/ ipfs路由
    -   [x] 用于名称的HTTP Gateway / ipns路由
    -   [ ] HTTP网关/ ipfs POST写入
    -   [ ] HTTP网关/ ipns PUT / POST写入
    -   [x] HTTP网关CORS和标头支持
-   [x] HTTP网关服务 (ipfs.io) 
    -   [x] HTTP网关服务: solarnet vps基础设施
    -   [x] HTTP网关服务: DNS架构
        -   [x] HTTP网关服务DNS: 部署在ipfs.io
        -   [x] HTTP网关服务DNS: dnslink,CNAME,A支持
        -   [ ] HTTP网关服务DNS: 区域自动化
        -   [ ] HTTP网关服务DNS: TLD冗余
    -   [x] HTTP网关服务: nginx前端
        -   [x] HTTP网关服务: 后端回退
        -   [x] HTTP网关服务: nginx阻止列表 (dmca) 
        -   [ ] HTTP网关服务: 速率限制
    -   [x] HTTP网关服务Devops
        -   [x] HTTP网关服务Devops: 容器
        -   [x] HTTP网关服务Devops: 自动部署
        -   [x] HTTP网关服务Devops: 日志记录
        -   [x] HTTP网关服务Devops: 事件监控
        -   [x] HTTP网关服务Devops: 状态警报
        -   [ ] HTTP网关服务Devops: 状态网页 (status.ipfs.io) 
        -   [ ] HTTP网关服务Devops: 混乱猴子
-   [x] HTTP网关自托管
    -   [x] HTTP网关自托管: ipfs.io项目网站
    -   [x] HTTP网关自托管: dist.ipfs.io
    -   [x] HTTP网关自托管: blog.ipfs.io
    -   [x] HTTP网关自托管: refs.ipfs.io

### IPFS分配

IPFS分配是IPFS项目计划的分配模型. 这意味着项目正式分发的所有程序的页面,源,二进制文件和链接的存储库. 

-   [x] IPFS分布: 架构
-   [ ] IPFS分配: 安全性
    -   [x] IPFS分发: HTTP站点的TLS证书
    -   [ ] IPFS分发: 代码签名
        -   [x] IPFS分发: 代码签名源
        -   [x] IPFS分发: 代码签名协议
        -   [x] IPFS发行版: 代码签名团队yubikeys
-   [x] IPFS分发: 网站
    -   [x] IPFS发行版: 网站设计
    -   [x] IPFS分发: 网站登陆页面
    -   [x] IPFS分发: 网站计划列表
    -   [x] IPFS发行版: 网站域名 (dist.ipfs.io) 
    -   [ ] IPFS发行版: 网站本地化
-   [x] IPFS分配: 工具
    -   [x] IPFS发行版: go-ipfs
    -   [x] IPFS分发: ipfs-update
    -   [x] IPFS分配: ipget
    -   [x] IPFS分配: fs-repo-migrations
    -   [x] IPFS分布: gx,gx-go
    -   [ ] IPFS分配: 站
    -   [ ] IPFS发行版: webui

### 安全

-   [ ] 为IPFS创建一个bug赏金计划
-   [ ] 让IPFS go和js实现完全审核
-   [ ] 创建安全工作组
-   [ ] 建立负责任的披露计划

### IPFS博客和时事通讯

为了让社区更新,我们运行了一个博客. 此博客通过IPFS本身以及电子邮件简报分发. 

-   [x] ipfs博客
    -   [x] 博客设计
    -   [x] 通过ipfs分发
    -   [x] blog.ipfs.io域名
    -   [ ] 使用POST数据结构
-   [x] 每周/通讯
    -   [x] 建立通讯流程
    -   [x] 突出贡献和贡献者
    -   [x] 发布到博客
-   [x] 电子邮件订阅
    -   [x] 使用tinyletter
    -   [x] 每周发布一次
    -   [ ] 发布博客
