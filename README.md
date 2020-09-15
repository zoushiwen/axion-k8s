## Oscar 部署k8s说明
 
> 本文工具支持部署
 - 单master多node节点k8s集群
 - 高可用多master多node节点k8s集群
 - 部署 ingress
 - ceph-rbd
 
 
 ### 部署前准备
 1、安装 ansible
 ~~~
 
 yum install -y ansible
 
 ~~~
 2、修改 config 文件
 
 ~~~
 
 如 ansible inventory 文件
 
 ~~~
 
 ### Plugin 插件
 ~~~
 1、 增加导入本机root用户的 ssh-key 到远程机器
 
 如果是非root用户执行，{{user}} 需要有sudo权限
 [root@q12471v axion-k8s]# ansible-playbook -i config -u {{user}} -k -K -b playbook/deploy_add_ssh_key.yml
 
 root用户执行
 [root@q12471v axion-k8s]# ansible-playbook -i config -k playbook/deploy_add_ssh_key.yml
 
 ~~~
 
 
