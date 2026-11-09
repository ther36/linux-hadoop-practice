# 问题：使用 yum 命令在CentOS 7 / 虚拟机里面下载文件失败

-  **环境**：CentOS 7 / 虚拟机
-  **现象**：yum install 报错 Could not resolve host: mirrorlist.centos.org，curl#6 错误。
-  **解决过程**：将 yum 源替换为阿里云镜像（Centos-7.repo），并执行 yum clean all && yum makecache。
-  **根因**：CentOS 7 于 2024 年 6 月 EOL，官方默认的 mirrorlist 域名停止解析，需要更换为国内镜像或 vault 归档源。
-  **一句话总结**：CentOS 7已经停止维护，必须用其他的来代替yum源。
<img width="1274" height="777" alt="abf31765418eda67172548cf83ca88aa" src="https://github.com/user-attachments/assets/4e7737a8-7cae-411d-9a89-d59abbb3b7dc" />
