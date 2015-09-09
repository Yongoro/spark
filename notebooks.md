## Some notebooks to use with Spark

	  http://zeppelin-project.org
	  [Jupyter](https://jupyter.org/), evolved from IPython project 
	*  [Data scientist workbench of IBM](https://datascientistworkbench.com/)
	*  [Scala notebook](https://github.com/Bridgewater/scala-notebook), based on the IPython notebook project 
	*  [Databricks cloud](https://databricks.com/product/databricks)

## Jupyter / IPython installation (ensure you have python 2.7 ++ or 3.3 ++ installed)
	
	### preparation [git, nodejs/npm, dev tools, python]
		#### installation of development tools and few extra libs.
		* yum -y install nodejs (npm/nodejs installation)
		* yum install git
		* yum groupinstall "Development tools"
		* yum install zlib-devel bzip2-devel openssl-devel ncurses-devel sqlite-devel readline-devel tk-devel 				gdbm-devel db4-devel libpcap-devel xz-devel
		* wget http://python.org/ftp/python/2.7.10/Python-2.7.10.tar.xz
		* tar xf Python-2.7.10.tar.xz
		* ./configure --prefix=/usr/local --enable-unicode=ucs4 --enable-shared LDFLAGS="-Wl,-rpath /usr/local/lib"
		* make && make altinstall 
		* cd Python-2.7.10
		
		#### Download and install Setuptools + pip (pip is a python package manager)
		* wget https://bitbucket.org/pypa/setuptools/raw/bootstrap/ez_setup.py(get setuptools setup' script)
		* python2.7 ez_setup.py (setuptools installation)
		* easy_install-2.7 pip (pip installation using setuptools)
		
		### pip syntax
		pip2.7 install [packagename]
		pip2.7 install --upgrade [packagename]
		pip2.7 uninstall [packagename]

		### python sandbox creation using virtualenv
		pip2.7 install virtualenv
		virtualenv-2.7 python27project (we create a sandbox named python27project)
		
		### check environment
		python --version (Result: Python 2.6.6)
		
		### sandbox activation
		source python27project/bin/activate
		python --version (Result: Python 2.7.10)
		deactivate (get out of the sandbox)
		
		notes:
		--enable-unicode=ucs4 (enable UTF-32 in Python 2.7)
		LDFLAGS="-Wl,-rpath /usr/local/lib" (compile the path into the executable)
		make altinstall (custom version of python; avoid having 2 python version with the same name)

	### install IPython
		pip install --upgrade setuptools pip
		pip install "ipython[all]"
		git clone https://github.com/jupyter/notebook.git
		cd notebook
		pip install --pre -e . (notebook installation)
		jupyter notebook (starting the notebook)

## Source markdown style
	
	* [markdown doc]: http://daringfireball.net/projects/markdown/syntax
	* http://www.cyberciti.biz/faq/rhel-centos-fedora-linux-yum-command-howto/
	* https://github.com/h2oai/h2o-2/wiki/Installing-python-2.7-on-centos-6.3.-Follow-this-sequence-exactly-for-centos-machine-only (more on python installation)
	* http://toomuchdata.com/2014/02/16/how-to-install-python-on-centos/
