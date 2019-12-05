1.将hbase通过Xftp传入Red-Hat
2.tar -zxvf hbase -C /usr/local (解压到目录下)
3.cd /usr/local/hbase/conf (到conf修改hbase-env.sh,hbase-site.xml)
4.vi hbase-env.sh
    4.1.set nu (方便查找)

    4.2.修改27行将jdk路径设置


export JAVA_HOME=/usr/local/jdk1.8.0_192
5.vi hbase-site.xml
    5.1.加入到<configuration></configuration>标签中




<property> 
<name>hbase.rootdir</name> 
<value>hdfs://node4:8020/hbase</value> 
</property>  
<property> <name>hbase.cluster.distributed</name> 
<value>false</value> 
</property>
6.vi /etc/profile
    6.1.设置变量

-stly



