Mac下安装vim环境步骤
1.将vimrc修改为.vimrc放置在用户根目录下
2.将vimrc.bundles修改为.vimrc.bundles放置在用户根目录下
3.vim打开.vimrc.bundles输入命令":BundleInstall"

说明：
如若出现以下报错：
报错Permission denied @ dir_s_mkdir - /usr/local/Frameworks
运行：

sudo mkdir /usr/local/Frameworks
sudo chown $(whoami):admin /usr/local/Frameworks



Ubuntu 下安装命令
