环境：64位Windows（7、8、10均可）

前提安装：Anaconda、Git。

从官网下载安装好Anaconda（选择Python2.7版本）及Git for Windows。


step1：clone 源码

在要存放xgboost的文件目录下打开git bash。

$ git clone --recursive https://github.com/dmlc/xgboost


step2：编译

编译可采取两种方式，一种是vs2013编译，一种是mingw64编译。但两种方式都要下载大体量安装包，在**网络限制或下载下来却配置失败**时，我们采用如下办法。

在xgboost官网推荐的网址处下载编译好的xgboost（主要下载 libxgboost.dll文件）。网址链接xgboost-windows-x64-binaries-for-download。


step3：install

window+R打开cmd命令行，这步主要是拷贝和安装。

copy libxgboost.dll (downloaded from this page) into the xgboost_install_dir\python-package\xgboost\ directory
cd xgboost_install_dir\python-package\
python setup.py install


step4：验证

window+R打开cmd命令行

python
>>>import xgboost

若无报错，则安装成功。若有，检查一下环境变量，把xgboost下的bin加入环境变量。
