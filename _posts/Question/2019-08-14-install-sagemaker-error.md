---
layout:     post
title:      "ERROR: Command errored out with exit status 1"
subtitle:   "rror in sagemaker setup command: 'extras_require' must be a dictionary "
date:       2019-08-14
author:     "Aili"
tags:
    - 数据科学
    -- 系统包安装
---

> 本篇为安装数据科学使用的包的过程中出现的错误

错误：

```bash 
 error in sagemaker setup command: 'extras_require' must be a dictionary whose values are strings or lists of strings containing valid project/version requirement specifiers.
    ----------------------------------------
ERROR: Command errored out with exit status 1: python setup.py egg_info Check the logs for full command output.
```
解决方案：
```bash
pip install --user --upgrade setuptools
```
测试成功，下面是测试实例过程。

``` bash

gouaili:~/Documents/sagemaker-python-sdk master$ sudo pip install sagemaker
Password:
DEPRECATION: Python 2.7 will reach the end of its life on January 1st, 2020. Please upgrade your Python as Python 2.7 won't be maintained after that date. A future version of pip will drop support for Python 2.7. More details about Python 2 support in pip, can be found at https://pip.pypa.io/en/latest/development/release-process/#python-2-support
WARNING: The directory '/Users/gouaili/Library/Caches/pip/http' or its parent directory is not owned by the current user and the cache has been disabled. Please check the permissions and owner of that directory. If executing pip with sudo, you may want sudo's -H flag.
WARNING: The directory '/Users/gouaili/Library/Caches/pip' or its parent directory is not owned by the current user and caching wheels has been disabled. check the permissions and owner of that directory. If executing pip with sudo, you may want sudo's -H flag.
Collecting sagemaker
  Downloading https://files.pythonhosted.org/packages/c4/10/bb581dcabd0228fba8bebade173b04fc971d1a81102af78a8af151030f25/sagemaker-1.36.4.tar.gz (210kB)
     |████████████████████████████████| 215kB 46kB/s 
    ERROR: Command errored out with exit status 1:
     command: /usr/bin/python -c 'import sys, setuptools, tokenize; sys.argv[0] = '"'"'/private/tmp/pip-install-fSquYD/sagemaker/setup.py'"'"'; __file__='"'"'/private/tmp/pip-install-fSquYD/sagemaker/setup.py'"'"';f=getattr(tokenize, '"'"'open'"'"', open)(__file__);code=f.read().replace('"'"'\r\n'"'"', '"'"'\n'"'"');f.close();exec(compile(code, __file__, '"'"'exec'"'"'))' egg_info --egg-base pip-egg-info
         cwd: /private/tmp/pip-install-fSquYD/sagemaker/
    Complete output (1 lines):
    error in sagemaker setup command: 'extras_require' must be a dictionary whose values are strings or lists of strings containing valid project/version requirement specifiers.
    ----------------------------------------
ERROR: Command errored out with exit status 1: python setup.py egg_info Check the logs for full command output.
gouaili:~/Documents/sagemaker-python-sdk master$ pip install --user --upgrade setuptools
DEPRECATION: Python 2.7 will reach the end of its life on January 1st, 2020. Please upgrade your Python as Python 2.7 won't be maintained after that date. A future version of pip will drop support for Python 2.7. More details about Python 2 support in pip, can be found at https://pip.pypa.io/en/latest/development/release-process/#python-2-support
Collecting setuptools
  Downloading https://files.pythonhosted.org/packages/75/b3/0a106dfaf7f48aef638da80b32608617cc8de4b24a22c8cd3759c32e5d30/setuptools-41.1.0-py2.py3-none-any.whl (576kB)
     |████████████████████████████████| 583kB 27kB/s 
Installing collected packages: setuptools
gouaili:~/Documents/sagemaker-python-sdk master$ sudo pip install sagemaker
DEPRECATION: Python 2.7 will reach the end of its life on January 1st, 2020. Please upgrade your Python as Python 2.7 won't be maintained after that date. A future version of pip will drop support for Python 2.7. More details about Python 2 support in pip, can be found at https://pip.pypa.io/en/latest/development/release-process/#python-2-support
WARNING: The directory '/Users/gouaili/Library/Caches/pip/http' or its parent directory is not owned by the current user and the cache has been disabled. Please check the permissions and owner of that directory. If executing pip with sudo, you may want sudo's -H flag.
WARNING: The directory '/Users/gouaili/Library/Caches/pip' or its parent directory is not owned by the current user and caching wheels has been disabled. check the permissions and owner of that directory. If executing pip with sudo, you may want sudo's -H flag.
Collecting sagemaker
  Downloading https://files.pythonhosted.org/packages/c4/10/bb581dcabd0228fba8bebade173b04fc971d1a81102af78a8af151030f25/sagemaker-1.36.4.tar.gz (210kB)
     |████████████████████████████████| 215kB 14kB/s 
Collecting boto3>=1.9.169 (from sagemaker)
  Downloading https://files.pythonhosted.org/packages/76/fb/3830e86db69775b1500d31d26d1dfcc83eada4af1627c14113168408431a/boto3-1.9.207-py2.py3-none-any.whl (128kB)
     |████████████████████████████████| 133kB 10kB/s 
Requirement already satisfied: numpy>=1.9.0 in /Library/Python/2.7/site-packages (from sagemaker) (1.16.4)
Collecting protobuf>=3.1 (from sagemaker)
  Downloading https://files.pythonhosted.org/packages/72/4a/23b02885d57d79368d805b2c6dccc70171ae9fd53a9fd28ebbb3c71fb0e2/protobuf-3.9.1-cp27-cp27m-macosx_10_9_intel.whl (1.4MB)
     |████████████████████████████████| 1.4MB 33kB/s 
Requirement already satisfied: scipy>=0.19.0 in /Library/Python/2.7/site-packages (from sagemaker) (1.2.2)
Requirement already satisfied: urllib3<1.25,>=1.21 in /Library/Python/2.7/site-packages/urllib3-1.22-py2.7.egg (from sagemaker) (1.22)
Collecting protobuf3-to-dict>=0.1.5 (from sagemaker)
  Downloading https://files.pythonhosted.org/packages/6b/55/522bb43539fed463275ee803d79851faaebe86d17e7e3dbc89870d0322b9/protobuf3-to-dict-0.1.5.tar.gz
Collecting docker-compose>=1.23.0 (from sagemaker)
  Downloading https://files.pythonhosted.org/packages/dd/e6/1521d1dfd9c0da1d1863b18e592d91c3df222e55f258b9876fa1e59bc4b5/docker_compose-1.24.1-py2.py3-none-any.whl (134kB)
     |████████████████████████████████| 143kB 29kB/s 
Collecting requests<2.21,>=2.20.0 (from sagemaker)
```
