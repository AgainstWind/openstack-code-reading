# nova-api源码阅读 #
nova项目代码较多，要阅读其代码，首先要熟openstack整体架构，以及nova基本功能和架构，
然后先从一个功能点开始比较方便上手。
首先从github下载最新的代码至本地（queue版本），了解下大致的目录结构。
对于一个python项目，我们首先要看的就是setup.py或setup.cfg。
通过setup.cfg文件entry_points找到代码入口：

    nova-api = nova.cmd.api:main

## 1.api.py ##
