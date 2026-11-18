# 低轨卫星负载均衡路由参考文献

本清单围绕老师提供的 TLR 论文整理。检索和 DOI 核验日期为 2026-11-18。选择原则是优先覆盖 TLR 的直接前驱、拥堵判断机制、队列/反向压力方法和近年负载均衡路由，而不是单纯罗列综述。

完整题录见 [references.bib](references.bib)，TLR 的机制拆解见 [tlr-reading-notes.md](tlr-reading-notes.md)。

## 首选阅读

| 编号 | 文献 | 与 TLR 的关系 | 开放全文 |
|---|---|---|---|
| R1 | G. Song, M. Chao, B. Yang, Y. Zheng, "TLR: A Traffic-Light-Based Intelligent Routing Strategy for NGEO Satellite IP Networks," *IEEE Transactions on Wireless Communications*, 13(6), 3380-3393, 2014. | 课程核心论文。联合判断当前节点队列与下一跳节点状态，动态调整预计算路径，并使用公共等待队列和防环机制。 | [DOI](https://doi.org/10.1109/TWC.2014.041014.130040)；课程提供本地 PDF |
| R2 | T. Taleb, D. Mashimo, A. Jamalipour, N. Kato, Y. Nemoto, "Explicit Load Balancing Technique for NGEO Satellite IP Networks With On-Board Processing Capabilities," *IEEE/ACM Transactions on Networking*, 17(1), 281-293, 2009. | TLR 的主要对比算法 ELB。根据下一跳或链路负载显式绕行，是课程中交通灯算法的直接基线。 | [DOI](https://doi.org/10.1109/TNET.2008.918084)；[机构记录](https://tohoku.repo.nii.ac.jp/records/66853) |
| R3 | J. Bai, X. Lu, Z. Lu, W. Peng, "Compact explicit multi-path routing for LEO satellite networks," *HPSR 2005*, 386-390. | TLR 引用的 CEMR。利用预期排队时延构造综合代价并预先选择多路径。 | [DOI](https://doi.org/10.1109/HPSR.2005.1503260) |
| R4 | Y. Rao, R. Wang, "Agent-based load balancing routing for LEO satellite networks," *Computer Networks*, 54(17), 3187-3195, 2010. | 用移动代理和指数遗忘估计队列时延，是 TLR 讨论的高开销分布式负载均衡方案。 | [DOI](https://doi.org/10.1016/j.comnet.2010.06.019) |
| R5 | H. Nishiyama, D. Kudoh, N. Kato, N. Kadowaki, "Load Balancing and QoS Provisioning Based on Congestion Prediction for GEO/LEO Hybrid Satellite Networks," *Proceedings of the IEEE*, 99(11), 1998-2007, 2011. | TLR 引用的预测式绕行机制，可在进入拥堵区域前提前分流。 | [DOI](https://doi.org/10.1109/JPROC.2011.2157885) |
| R6 | H. Wang, G. Wen, N. Liu, J. Zhang, Y. Tao, "A load balanced routing algorithm based on congestion prediction for LEO satellite networks," *Cluster Computing*, 22(S4), 8025-8033, 2017. | 比 TLR 更近的 LEO 拥塞预测实例，可用于比较预测周期和门限设置。 | [DOI](https://doi.org/10.1007/s10586-017-1579-8) |
| R7 | X. Xu, C. Dong, A. Liu, "Optimization of load balancing routing algorithm based on extended localized link states in low earth orbit satellite networks," *International Journal of Satellite Communications and Networking*, 39(6), 591-604, 2021. | 利用扩展局部链路状态与触发式拥塞通知，解决只看下一跳造成的局部最优问题。 | [DOI](https://doi.org/10.1002/sat.1403) |
| R8 | C. Han, W. Xiong, R. Yu, "Load-Balancing Routing for LEO Satellite Network with Distributed Hops-Based Back-Pressure Strategy," *Sensors*, 23(24), 9789, 2023. | 分布式跳数反向压力，直接对应课程中的队列状态与备用下一跳问题。 | [PDF](pdfs/10.3390_s23249789.pdf) |

## 扩展阅读

| 编号 | 文献 | 关注点 | 开放全文 |
|---|---|---|---|
| R9 | W. Liu, Y. Tao, L. Liu, "Load-Balancing Routing Algorithm Based on Segment Routing for Traffic Return in LEO Satellite Networks," *IEEE Access*, 7, 112044-112053, 2019. | 分段路由与回程业务负载均衡。 | [PDF](pdfs/10.1109_ACCESS.2019.2934932.pdf) |
| R10 | J. Liu, R. Luo, T. Huang, C. Meng, "A Load Balancing Routing Strategy for LEO Satellite Network," *IEEE Access*, 8, 155136-155144, 2020. | 较新的 LEO 负载均衡路由设计，可作为工程实现参照。 | [PDF](pdfs/10.1109_ACCESS.2020.3017615.pdf) |
| R11 | C. Dong, X. Xu, A. Liu, X. Liang, "Load balancing routing algorithm based on extended link states in LEO constellation network," *China Communications*, 19(2), 247-260, 2022. | 扩展链路状态和星座网络负载感知。 | [DOI](https://doi.org/10.23919/JCC.2022.02.020) |
| R12 | X. Deng, L. Chang, S. Zeng, L. Cai, J. Pan, "Distance-Based Back-Pressure Routing for Load-Balancing LEO Satellite Networks," *IEEE Transactions on Vehicular Technology*, 72(1), 1240-1253, 2023. | 距离约束与反向压力结合，可用于设计队列差代价。 | [DOI](https://doi.org/10.1109/TVT.2022.3206616) |
| R13 | Y. Zhou, H. Chen, Z. Dou, "MOLM: Alleviating Congestion through Multi-Objective Simulated Annealing-Based Load Balancing Routing in LEO Satellite Networks," *Future Internet*, 16(4), 109, 2024. | 同时考虑时延与路径稳定性，采用多目标优化处理拥堵节点。 | [PDF](pdfs/10.3390_fi16040109.pdf) |
| R14 | J. Sun, E. Modiano, "Routing Strategies for Maximizing Throughput in LEO Satellite Networks," *IEEE Journal on Selected Areas in Communications*, 22(2), 273-286, 2004. | 传播时延最短路导致容量瓶颈的经典背景文献。 | [DOI](https://doi.org/10.1109/JSAC.2003.819975) |
| R15 | I. F. Akyildiz, E. Ekici, M. D. Bender, "MLSR: a novel routing algorithm for multilayered satellite IP networks," *IEEE/ACM Transactions on Networking*, 10(3), 411-424, 2002. | 多层卫星网络路由的经典工作，用于理解早期拓扑与负载均衡假设。 | [DOI](https://doi.org/10.1109/TNET.2002.1012371) |

## 建议使用方法

1. 组内基础报告至少精读 R1、R2、R3、R7 和 R8，覆盖 TLR、显式负载均衡、多路径、局部链路状态和反向压力。
2. 实现 TLR 简化版时，优先保留当前队列和下一跳状态的组合判断，并明确删去哪些轨道预计算、通知协议和公共队列细节。
3. 做结果讨论时，用 R7 解释只看下一跳的局部最优问题，用 R12、R8 解释队列差和反向压力，用 R13 讨论路径稳定性这一额外维度。
4. 引用格式统一使用 [references.bib](references.bib)。

## 版权说明

`pdfs/` 中只收录出版社或开放获取记录明确标注 Creative Commons Attribution 4.0（CC BY 4.0）的论文。R1 的课程 PDF 带有 IEEE Xplore 机构下载和再分发限制，因此没有加入公开仓库。其他非开放论文只提供 DOI 或出版社入口。

