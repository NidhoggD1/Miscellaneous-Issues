# pip默认源

https://pypi.org/simple

# conda默认源

https://repo.anaconda.com/pkgs/main

https://repo.anaconda.com/pkgs/r

https://repo.anaconda.com/pkgs/msys2

# pip永久换源

pip config set global.index-url 新源URL

## 常用源

清华: https://pypi.tuna.tsinghua.edu.cn/simple

阿里: https://mirrors.aliyun.com/pypi/simple/

豆瓣: https://pypi.douban.com/simple/

# conda永久换源

创建 *.condarc* 文件于 *'C:\Users\UserName\ .condarc'*：

conda config --set show_channel_urls yes

替换内容（任一即可）：

北京外国语大学开源软件镜像站

channels:
  - defaults
show_channel_urls: true
channel_alias: https://mirrors.bfsu.edu.cn/anaconda
default_channels:
  - https://mirrors.bfsu.edu.cn/anaconda/pkgs/main
  - https://mirrors.bfsu.edu.cn/anaconda/pkgs/free
  - https://mirrors.bfsu.edu.cn/anaconda/pkgs/r
  - https://mirrors.bfsu.edu.cn/anaconda/pkgs/pro
  - https://mirrors.bfsu.edu.cn/anaconda/pkgs/msys2
custom_channels:
  conda-forge: https://mirrors.bfsu.edu.cn/anaconda/cloud
  msys2: https://mirrors.bfsu.edu.cn/anaconda/cloud
  bioconda: https://mirrors.bfsu.edu.cn/anaconda/cloud
  menpo: https://mirrors.bfsu.edu.cn/anaconda/cloud
  pytorch: https://mirrors.bfsu.edu.cn/anaconda/cloud

上海交通大学开源软件镜像站

channels:
  - defaults
show_channel_urls: true
channel_alias: https://anaconda.mirrors.sjtug.sjtu.edu.cn/
default_channels:
  - https://anaconda.mirrors.sjtug.sjtu.edu.cn/pkgs/main
  - https://anaconda.mirrors.sjtug.sjtu.edu.cn/pkgs/free
  - https://anaconda.mirrors.sjtug.sjtu.edu.cn/pkgs/mro
  - https://anaconda.mirrors.sjtug.sjtu.edu.cn/pkgs/msys2
  - https://anaconda.mirrors.sjtug.sjtu.edu.cn/pkgs/pro
  - https://anaconda.mirrors.sjtug.sjtu.edu.cn/pkgs/r
custom_channels:
  conda-forge: https://anaconda.mirrors.sjtug.sjtu.edu.cn/conda-forge
  soumith: https://anaconda.mirrors.sjtug.sjtu.edu.cn/cloud/soumith
  bioconda: https://anaconda.mirrors.sjtug.sjtu.edu.cn/cloud/bioconda
  menpo: https://anaconda.mirrors.sjtug.sjtu.edu.cn/cloud/menpo
  viscid-hub: https://anaconda.mirrors.sjtug.sjtu.edu.cn/cloud/viscid-hub

阿里巴巴开源软件镜像站

channels:
  - defaults
show_channel_urls: true
default_channels:
  - http://mirrors.aliyun.com/anaconda/pkgs/main
  - http://mirrors.aliyun.com/anaconda/pkgs/r
  - http://mirrors.aliyun.com/anaconda/pkgs/msys2
custom_channels:
  conda-forge: http://mirrors.aliyun.com/anaconda/cloud
  msys2: http://mirrors.aliyun.com/anaconda/cloud
  bioconda: http://mirrors.aliyun.com/anaconda/cloud
  menpo: http://mirrors.aliyun.com/anaconda/cloud
  pytorch: http://mirrors.aliyun.com/anaconda/cloud
  simpleitk: http://mirrors.aliyun.com/anaconda/cloud

清华大学开源软件镜像站

channels:
  - defaults
show_channel_urls: true
channel_alias: https://mirrors.tuna.tsinghua.edu.cn/anaconda
default_channels:
  - https://mirrors.tuna.tsinghua.edu.cn/anaconda/pkgs/main
  - https://mirrors.tuna.tsinghua.edu.cn/anaconda/pkgs/free
  - https://mirrors.tuna.tsinghua.edu.cn/anaconda/pkgs/r
  - https://mirrors.tuna.tsinghua.edu.cn/anaconda/pkgs/pro
  - https://mirrors.tuna.tsinghua.edu.cn/anaconda/pkgs/msys2
custom_channels:
  conda-forge: https://mirrors.tuna.tsinghua.edu.cn/anaconda/cloud
  msys2: https://mirrors.tuna.tsinghua.edu.cn/anaconda/cloud
  bioconda: https://mirrors.tuna.tsinghua.edu.cn/anaconda/cloud
  menpo: https://mirrors.tuna.tsinghua.edu.cn/anaconda/cloud
  pytorch: https://mirrors.tuna.tsinghua.edu.cn/anaconda/cloud
  simpleitk: https://mirrors.tuna.tsinghua.edu.cn/anaconda/cloud

然后运行

conda clean -i 

# conda恢复默认源

conda config --remove-key channels

或

直接删除 *'C:\Users\UserName\ .condarc'*

或

运行

conda config --add channels https://repo.anaconda.com/pkgs/main

conda config --add channels https://repo.anaconda.com/pkgs/r

conda config --add channels https://repo.anaconda.com/pkgs/msys2

conda config --set show_channel_urls yes

# 临时换源

xxx install -i url


