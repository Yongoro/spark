## Some notebooks to use with Spark

	* [zeppelin](http://zeppelin-project.org/)
	* [Jupyter](https://jupyter.org/), evolved from IPython project 
	* [Data scientist workbench of IBM](https://datascientistworkbench.com/)
	* [Scala notebook](https://github.com/Bridgewater/scala-notebook), based on the IPython notebook project 
	* [Databricks cloud](https://databricks.com/product/databricks)

## IPython installation (ensure you have python 2.7 ++ or 3.3 ++ installed)

	### install python 2.7 (maintaining the previous python's version)
		$cd /usr/src
		$wget https://www.python.org/ftp/python/2.7.10/Python-2.7.10.tgz
		$tar xzvf Python-2.7.10.tgz
		$cd Python-2.7.10
		$ ./configure
		$make altinstall (used to prevent replacing the default python binary file /usr/bin/python)
		
		* we have to create an alias *
		$echo 'alias python="/usr/bin/pip-python"' >> $HOME/.bashrc
		$source $HOME/.bashrc
		
	### turn on EPEL repo
		$cd /tmp
		$wget http://mirrors.ircam.fr/pub/fedora/epel/epel-release-latest-6.noarch.rpm
		#rpm -ivh epel-release-latest-6.noarch.rpm or #yum install epel-release-latest-6.noarch.rpm
		
	### install pip
		#yum -y install python-pip
		
	### install IPython
		$ pip install "ipython[all]"

## Jupyter installation
	
		
		
## Source markdown style
	
	* [markdown doc]: http://daringfireball.net/projects/markdown/syntax
	* http://www.cyberciti.biz/faq/rhel-centos-fedora-linux-yum-command-howto/
	* https://github.com/h2oai/h2o-2/wiki/Installing-python-2.7-on-centos-6.3.-Follow-this-sequence-exactly-for-centos-machine-only (more on python installation)
