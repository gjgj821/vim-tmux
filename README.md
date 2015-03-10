### 保存配置`vim`及`tmux`的配置文件
> 使用Vundle管理vim插件，既方便有省心，我们只需维护好.vimrc文件，便很方便的管理，更新vim插件。

## 一.使用方法：
```
cd ~
git clone https://github.com/gjgj821/vim-tmux.git 
```

# `vim`：
```
git clone https://github.com/gmarik/vundle.git ~/.vim/bundle/vundle
cp vim-tmux/.vimrc ~
cp -r vim-tmux/.vim ~
```
# 安装插件
打开`vim `
在`vim`命令行输入`:BundleInstall`,回车，开始下载vimrc配置中的插件

# `powerline`
https://powerline.readthedocs.org/en/latest/installation/linux.html#fonts-installation

# `tmux`：
```
cp -r vim-tmux/.tmux ~
git clone https://github.com/erikw/tmux-powerline.git
cp -r tmux-powerline ~/.tmux
cp vim-tmux/.tmux.conf ~/.tmux.conf
cp vim-tmux/.tmux-powerlinerc ~/.tmux-powerlinerc
```

## 二.`vim`可能存在的问题：
1. `powerline`乱码问题: https://powerline.readthedocs.org/en/latest/index.html

2. `Command-t`安装问题
错误：`require’: no such file to load — mkmf (LoadError)'
```
mkmf.rb is part of the “ruby1.8-dev” package. 
sudo apt-get install ruby1.8-dev
```

3. `Qfixtoggle`错误
QFixToggle/plugin/qfixtoggle.vim为DOS格式，需要转换为unix格式
```
sudo apt-get install dos2unix
dos2unix ~/.vim/bundle/QFixToggle/plugin/qfixtoggle.vim
```

4. `NerdTree`错误
NerdTree中添加了tag的打开
需要安装Exuberant Ctags
`sudo apt-get install exuberant-ctags`

5)全屏切换需要安装`wmctrl`
`sudo apt-get install wmctrl`
`F11`即可

## 三.`tmux`可能遇到的问题
1. 进入后没有任何改变
有可能`tmux`没有加载配置文件
`tmux source-file ~/.tmux.conf`

2. 状态栏为空
脚本执行错误
```
~/.tmux/tmux-powerline/powerline.sh left
~/.tmux/tmux-powerline/powerline.sh right
```
安装`curl`
`sudo apt-get install curl`


## 四.`Vundle`说明
1.`Vundle`介绍
项目托管在github上 https://github.com/gmarik/vundle
其特色在于使用git来管理插件,更新方便，支持搜索，一键更新，从此只需要一个vimrc走天下.

2.安装与配置
使用git命令
```
$ git clone https://github.com/gmarik/vundle.git ~/.vim/bundle/vundle
```

> windows下使用，可以考虑放置在$HOME/.vim/bundle/vundle

## 五.Windows下使用的配置文件
