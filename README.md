## 使用spf13的vim配置，在此基础上做个性化的配置

https://github.com/spf13/spf13-vim

# 1.首先安装
```
sh <(curl https://j.mp/spf13-vim3 -L)>
```
说明:
1. 将系统中的.vim软链接到spf13-vim3版本库
2. 自动安装vbundle的插件
3. 个性化设置可以添加在以下3个文件中
    * .vimrc.before.local  :在bundles之前,可以移出默认的bundle,提供了unbundle函数
    * .vimrc.bundles.local :在bundles之后,系统设置之前,可以关闭某些系统设置
    * .vimrc.local         :添加自定义的按键绑定

# 2.spf13的按键说明
* leader : `,`
* `<leader> / `: 搜索高亮开关
* `<leader> ff`: 快速搜索当前游标所在的变量
