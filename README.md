# Task_11.1
Configuring hadoop cluster (NameNode and DataNode) using Ansible.

In this article we are performing 2 Tasks

**Task 1**: Configuring Hadoop

**Task 2**: Start Cluster services using Ansible Playbook

Lets get to task 1 first, To accomplish Task 1 follow the steps below :

**Step 1**: Install the required software.

To use Hadoop service we first need to install **hadoop** software, prior to that the hadoop requires **java development kit** to function. So, we have to install JDK first and then Hadoop.

**Note: Commands are for RHEL8 Linux**

```
rpm -i jdk-8u171-linux-x64.rpm   
```
Now install hadoop
```
rpm -i hadoop-1.2.1-1.x86_64.rpm
```

if the above command fails it might because of some file in hadoop and jdk conflicts. so to solve this issue without going into technicalities we sometimes need to install hadoop focefully
```
rpm -i hadoop-1.2.1-1.x86_64.rpm --force
```
after installing both the software.

Its time to configure hadoop and to do so goto directory of hadoop "/etc/hadoop".

now configure the system according to the need i.e weather we want a NameNode or DataNode.

 **NAMENODE** : NameNode.yml

 **DATANODE** : datanode.yml

Copy the appropriate configuration file in the ManagedNode at location /etc/hadoop.

copy the hdfs and core file for either NameNode or DataNode according to the requirement in the managed node.
