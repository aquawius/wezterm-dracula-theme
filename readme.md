## 这是一个我自己的wezterm配置文件

### 使用方法

1. 将本仓库拷贝

``` powershell
git clone https://gitee.com/aquawius/wezterm-config.git
```

2. 将拷贝的文件放在 `C:/Users/用户名/.config/`下

> ##### 完整文件结构应该这样
>
> ``` powershell
> 
> C:\USERS
> ├─Public
> ├─QU(你的用户名)
> │  ├─Documents
> │  ├─Downloads
> │  ├─Music
> │  ├─Pictures
> │  ├─Videos
> │  ├─.config
> │  │  ├─git
> │  │  └─wezterm
> │  │     └─.git   (delete it)
> │  │     dracula.lua
> │  │     readme.md
> │  │     wezterm.lua
> │  │        ...
> ```

3. 完成!

### 后记

> ##### 关于终端
>
> > 这里默认使用的终端是`powershell 7`,你可以更改为任意类型的终端,比如`cmd.exe`, `powershell 5(powershell.exe)`, `powershell 7(pwsh.exe)`
> >
> > 修改方式是在`./config/wezterm/wezterm.lua`中找到
> > `default_prog = { 'pwsh' },` 将`{ }`中的`'pwsh'`改为你想要的终端 (绝对路径或者环境变量都可以)
>
> ###### 主题配色
>
> > 原本是我自己写的配置,用的自带的Sukura配色加上自己写的tab栏, 现在的配置文件改为使用[dracula官方提供的配色](https://github.com/dracula/wezterm.git)
> >
> > 原来的
> >
> > ![img](readme.assets/2283725-20220726143424695-1970924268.png)
> >
> > dracula官方提供的配色
> >
> > ![image-20220810020054548](readme.assets/image-20220810020054548.png)
> >
> > 怎么说,还是Dracula好看!  Dracula yyds!