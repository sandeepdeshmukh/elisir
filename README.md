# Setting up Hadoop and other softwares for Elixir Professional Services - Big Data and Hadoop training

Download the tar ball  https://drive.google.com/open?id=0B5BbiPqrIgf8QkRFUTk2cnl6eVk . By default it will be saved in Downloads directory.
Run following commands

```bash
cd $HOME # Takes you to your home directory
tar -zxvf \<hadoop.tgz path - mostly ~/Downloads/hadoop.tgz\> 
```

Edit your .bashrc file and add following lines at the end

```bash
gedit .bashrc
```

export JAVA_HOME=/usr/lib/jvm/java-1.8.0-openjdk-amd64/

export HADOOP_HOME=$HOME/hadoop/hadoop-2.7.2/

PATH=$PATH:$HADOOP_HOME/bin/:$HADOOP_HOME/sbin/:$HOME/hadoop/bin/

Now go to the following hadoop configuration directory and replace elixir word with your login name.
```bash
cd $HOME/hadoop/hadoop-2.7.2/etc/hadoop
 sed -i ~s/elixir/<YOUR_USER_NAME>/g *
```

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
If there is no error in the last command, and you see input directory as the output, congratulate yourself for setting up the Hadoop successfully.

