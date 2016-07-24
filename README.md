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
cat ~/.ssh/id_rsa.pub >> ~/.ssh/authorized_keys
```

Format HDFS and check if that is working fine.
```bash
hdfs namenode -format
start-hadoop.sh
hdfs dfs -mkdir -p input
hdfs dfs -ls 
```
