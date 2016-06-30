# Setting up Hadoop and other softwares for
# Exixir Professional Services - Big Data and Hadoop trainign

Run following commands

cd $HOME
tar -zxvf <elixir.tgz path> 

source $HOME/hadoop/elixir.sh

ssh-keygen

cat ~/.ssh/id_rsa.pub >> ~/.ssh/authorized_keys

hdfs namenode -format

start-hadoop.sh

hmkdir -p input

hls

