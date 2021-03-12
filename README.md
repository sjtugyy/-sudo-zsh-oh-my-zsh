# -sudo-zsh-oh-my-zsh

## 安装ncurses 
```bash
cd ../../ && mkdir ncurses && cd ncurses  # 切换到上级目录新建ncurses文件夹
wget http://ftp.gnu.org/pub/gnu/ncurses/ncurses-6.1.tar.gz  # 下载最新版本ncurses
tar -xzvf ncurses-6.1.tar.gz  # 解压
cd ncurses-6.1
./configure --prefix="绝对路径(我安装在了 ncurses/ 下)" --with-shared --without-debug --enable-widec  # 指定路径configure
make && make install  # 安装
```

## 安装zsh

```bash
wget -O zsh.tar.xz https://sourceforge.net/projects/zsh/files/latest/download

# 解压，这里下载下来的是xz格式，要先用xz解压一遍，再用tar解压。
xz -d zsh.tar.xz
tar -xf zsh.tar 
cd zsh-5.7.1        # 注意这个版本号要根据自己的实际情况来

# 配置与编译。--prefix选项指定安装目录
./configure --prefix=$HOME/Applications/zsh-5.7.1   
make
make install
```
