Mac下安装vim环境步骤
1.将vimrc修改为.vimrc放置在用户根目录下
2.将vimrc.bundles修改为.vimrc.bundles放置在用户根目录下
3.vim打开.vimrc.bundles输入命令":BundleInstall"

说明：
1.如若出现以下报错：
报错Permission denied @ dir_s_mkdir - /usr/local/Frameworks
运行：
sudo mkdir /usr/local/Frameworks
sudo chown $(whoami):admin /usr/local/Frameworks


2.重新编译YCM(YouCompleteMe)方法

YouCompleteMe unavailable: dlopen(/Library/Frameworks/Python.framework/Versions/2.7/lib/python2.7/
lib-dynload/_io.so, 2): Symbol not found: __PyCodecInfo_GetIncrementalDecoder
  Referenced from: /Library/Frameworks/Python.framework/Versions/2.7/lib/python2.7/lib-dynload/_io
.so
  Expected in: flat namespace
 in /Library/Frameworks/Python.framework/Versions/2.7/lib/python2.7/lib-dynload/_io.so

 mac 升级后是10.12，vim版本是7.4.898,在vim中输入

:py import sys; print(sys.version)


2.7.10 (default, Feb 22 2019, 21:55:15)
[GCC 4.2.1 Compatible Apple LLVM 10.0.1 (clang-1001.0.37.14)]

而我在mac上又装了python2.7.13，编译YCM的时候用的也是2.7.13，所以才会出现这种错误，我于是从python官网上重新下载2.7.10，安装以后,终端输入
python --version

再重新编译YCM 就可以解决上述问题。


brew install python@2
cd ~/.vim/bundle/YouCompleteMe
python2 ./install.py --clang-completer


cd ~/.vim/bundle/YouCompleteMe 
./install.py --clang-completer 

3. 清除列表中没有的插件
:BundleClean

Ubuntu 下安装命令
