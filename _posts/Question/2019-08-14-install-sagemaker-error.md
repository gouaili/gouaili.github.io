---
layout:     post
title:      "ERROR: Command errored out with exit status 1"
subtitle:   "rror in sagemaker setup command: 'extras_require' must be a dictionary "
date:       2019-08-14
author:     "Aili"
catalog: true
tags:
    - 系统安装
---

> 本篇为该系列第一篇 —— 行业与战略，让我们聊聊行业、战略与格局。

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
