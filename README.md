# Setting up Hadoop and other softwares for Elixir Professional Services - Big Data and Hadoop training

Download the tar.gz file : [https://drive.google.com/open?id=0B5BbiPqrIgf8MlJwaWxqQmJlaUE]

Run following commands

cd $HOME

tar -zxvf \<elixir.tgz path\> 

source $HOME/hadoop/elixir.sh

ssh-keygen

cat ~/.ssh/id_rsa.pub >> ~/.ssh/authorized_keys

hdfs namenode -format

start-hadoop.sh

hmkdir -p input

hls

