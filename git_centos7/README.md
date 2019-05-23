# Centos7搭建git

## 一、依赖库安装

yum install curl-devel expat-devel gettext-devel openssl-devel zlib-devel

yum install gcc perl-ExtUtils-MakeMaker

#卸载低版本的 Git

yum remove git

#下载git-2.21.0

make prefix=/usr/local/git all #编译时间很长

make prefix=/usr/local/git install



ln -s /usr/local/git/bin/git-upload-pack /usr/bin/git-upload-pack 

ln -s /usr/local/git/bin/git-receive-pack /usr/bin/git-receive-pack 



groupadd git

useradd git -g git

passwd git  #参数是用户名

su - git  //切换git用户



https://blog.csdn.net/wugenqiang/article/details/81215396

ssh-keygen -t rsa -C “gdnh_16@163.com”



//端口在22的情况下
git clone git@154.8.235.117:/home/gitrepo/hiynn.git



//端口在非22的情况下（如5000）
git clone ssh://git@154.8.235.117:5000/home/git/hiynn.git



修改git密码



