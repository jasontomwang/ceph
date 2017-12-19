# ceph
ceph deployment for ubuntu 16.04

ceph集群的网络架构（此处有两张网络）：

第一张为所有节点的eth0接口，用于客户端读写传输数据
第二张为所有节点的eth1接口，用于各osd节点之间同步数据、发送心跳信息等

本测试集群共有8个节点：
1个部署节点  ceph-dep
3个MON节点
3个OSD节点   每个osd节点有一块硬盘/dev/vdb用于osd，将此硬盘分为8个区，前4个区为osd，后4个区为journal
2个client节点

