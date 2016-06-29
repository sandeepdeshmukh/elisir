# Setting up Hadoop and other softwares for
# Exixir Professional Services - Big Data and Hadoop trainign

Run following commands

tar -zxvf elixir.tgz 

source ~/hadoop/elixir.sh

ssh-keygen

cat ~/.ssh/id_rsa.pub >> ~/.ssh/authorized_keys

hdfs namenode -format

start-hadoop.sh

hmkdir -p input

hls

