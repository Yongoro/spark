#Getting started with spark

##Installation of spark in standalone mode on CentOS 6.6
    * install CentOS 6.6 with Desktop version
    * download spark-1.4.1-bin-hadoop2.6.tgz (prebuild for hadoop 2.6 +) 
          $wget http://wwwftp.ciril.fr/pub/apache/spark/spark-1.4.1/spark-1.4.1-bin-hadoop2.6.tgz
    * unzip
          $tar -xvf spark-1.4.1-bin-hadoop2.6.tgz

##Prerequisites
    * install java 
        $java -version (1.7.0_85) -- version
        $sudo yum install java-1.7.0-openjdk-devel
        $find / -name java        -- to know where it's installed and note the path
    
    * enable JAVA_HOME environnement variable for all users, persistently [create java.sh file under /etc/profile.d]  
        $vim /etc/profile.d/java.sh
        
        ** script's content **
        #!/bin/bash
        export JAVA_HOME=/usr/lib/jvm/java-1.7.0-openjdk-1.7.0.85.x86_64
        export PATH=$JAVA_HOME/bin:$PATH
        
        ** make it executable **
        $chmod +x /etc/profile.d/java.sh
        
        ** load environnement variable in java.sh without restarting machine **
        $source /etc/profile.d/java.sh
      
        ** test **
        $java -version
        
      other method
      
        $vim $HOME/.bashrc
            + add the above two exports
        $source $HOME/.bashrc
      
    * install git
        $yum install git
        
    * download compatible scala (spark 1.4.1 --> scala 2.10.x)
    * set variable SCALA_HOME

###resources
    [official spark documentation](http://spark.apache.org/docs/latest/)
    [spark standalone](https://spark.apache.org/docs/latest/spark-standalone.html)
