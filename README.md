# Setting up Hadoop and other softwares for Elixir Professional Services - Big Data and Hadoop training

Download the tar.gz file : [https://drive.google.com/open?id=0B5BbiPqrIgf8MlJwaWxqQmJlaUE]

Run following commands

```bash
cd $HOME # Takes you to your home directory
wget < file -link>
tar -zxvf \<hadoop.tgz path\> 
```

Edit your .bashrc file and add following lines at the end

```bash
nano .bashrc
```

export JAVA_HOME=/usr/lib/jvm/java-1.8.0-openjdk-amd64/

export HADOOP_HOME=$HOME/hadoop/hadoop-2.7.2/

PATH=$PATH:$HADOOP_HOME/bin/:$HADOOP_HOME/sbin/:$HOME/hadoop/bin/

Now setup the passwordless ssh for your login
```bash
ssh-keygen
Generating public/private rsa key pair.
Enter file in which to save the key (/home/elixir/.ssh/id_rsa): 
Created directory '/home/elixir/.ssh'.
Enter passphrase (empty for no passphrase): 
Enter same passphrase again: 
Your identification has been saved in /home/elixir/.ssh/id_rsa.
Your public key has been saved in /home/elixir/.ssh/id_rsa.pub.
The key fingerprint is:
SHA256:3JHop0oTKd3488b3TR6HAxUU8W1zav1QkGQL3KnD/wE elixir@1511250d0578
The key's randomart image is:
+---[RSA 2048]----+
|           ..+O= |
|         . ..o+=.|
|        . o. .o.*|
|     . * . .+E =o|
|    . = S o .o= .|
|     . o o   o.+.|
|      o +.    oo=|
|     . o oo .  =+|
|      .  ... .. o|
+----[SHA256]-----+
```

Last step in setting ssh key
```bash
cat ~/.ssh/id_rsa.pub >> ~/.ssh/authorized_keys
```

Format HDFS and check if that is working fine.
```bash
hdfs namenode -format
start-hadoop.sh
hdfs dfs -mkdir -p input
hdfs dfs -ls 
```
