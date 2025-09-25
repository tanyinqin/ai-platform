# ai-platform
本人在ubuntu24.04上部署ollama+大模型+openwebui+ragflow+n8n的配置文件和使用方法的分享，节约部署排错的时间成本，我没有显卡，只能用cpu版本，如果需要用gpu自行参考改代码
主机环境
ubuntu24.04 桌面版
ip地址:192.168.0.48
cpu：12核心24线程
内存：24G
显卡：最好能有显卡，本人无米，暂时没配，cpu版比较慢，反应迟钝，
网络环境：局域网代理，后者自行购买机场局域网代理，方便拉取镜像和github找对应文档
硬盘配置：sda:120G 安装系统，保持空余磁盘空间 内存不足方便调用磁盘模拟内存使用
                sdb:300G 安装docker+composer，容器镜像,ollama,openwebui,ragflow,n8n，大模型需要按需拉取
1.安装系统自行查找有很多网上教程，安装openssh-server，第三方ssh软件连接，不赘述了
2.新建磁盘并挂载sdb1挂载目录/mnt/data/
3.设置代理上网
4.安装Docker+compose
5.设置全局代理上网，包括docker拉镜像也需要代理上网
6.上github下载ragflow的zip文件,镜像地址：https://github.com/infiniflow/ragflow
7.解压缩文件拷贝docker里的nginx文件夹所有文件，.env上,和我修改的docker-compose.yml传到宿主安装目录
8.运行docker compose up -d
9.docker ps查看容器情况
10.RAGFlow: http://你的IP地址:9380 或 http://你的IP地址:80
     Open WebUI: http://你的IP地址:3000
      n8n: http://你的IP地址:5670
11.使用方法只能自行研究没有捷径本人只希望在安装部署的环节为大家节约学习的时间成本和排错成本
