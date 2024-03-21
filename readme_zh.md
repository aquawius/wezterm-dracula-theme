## 这是一个我自己的[wezterm](https://wezfurlong.org/wezterm/)配置文件

> 又一个基于[dracula](https://draculatheme.com/)配色方案的[wezterm](https://wezfurlong.org/wezterm/)配置文件，增加了一些有用的功能。

![gif](./readme.assets/feature_preview.gif)

### ✅ 特性

-  Dracula 配色方案。
-  美观的底部状态栏。
-  支持快速启动各种环境。（需要调整配置文件）

### :art: 一些截图

![Screenshot1](./readme.assets/PixPin_2024-03-20_17-07-36.png)

![Screenshot2](./readme.assets/PixPin_2024-03-20_17-08-35.png)

---

### 🔨 开始配置

1. ##### 切换至你的 `homedir/.config/` 文件夹。

    ```
    cd C:/Users/ `username` /.config/
    ```

    > （如果没有 `.config` 文件夹，请创建一个）

2. ##### 克隆仓库。

    ```shell
    git clone https://github.com/aquawius/wezterm-config.git
    ```

3. ##### 将 `wezterm-config` 重命名为 `wezterm`。

    ```shell
    C:\USERS
    ├─Public
    ├─QU（你的主目录）
    │  ├─Documents
    │  ├─Downloads
    │  ├─Pictures
    │  ├─.config
    │  │  ├─git
    │  │  └─wezterm	（将 wezterm-config 重命名为 wezterm）
    │  │     └─.git
    │  │     dracula.lua
    │  │     readme.md
    │  │     wezterm.lua
    │  │        ...
    ```

4. ##### 完成

欢迎提PR或Issue 😊

### :pushpin: 使用方法

您可以在终端底部找到一个 `+`。

> 单击 `+` 创建一个默认终端。（pwsh.exe）
>
> 右键单击 `+` 选择，您应该看到一个列出所有终端的列表
>
> ![right_click_to_open_list](./readme.assets/right_click_list.gif)
>
> 中键单击选定的选项卡关闭此选项卡。
>
> ![middle_click_to_close_tab](./readme.assets/middleclick_toclose.gif)

------

### :speech_balloon: 你应该知道的东西

1. 配置的默认字体是 [CascadiaCode nerd font](https://www.programmingfonts.org/#cascadia-code)，您可以在此链接中下载：https://www.nerdfonts.com/font-downloads。

2. 默认 shell 是 `powershell7`（pwsh.exe），在 Linux 上是 `fish`。如果您没有这些 shell (或者你不想使用这些shell)，您可以在注释以下行：

    > 更改默认 shell：
    >
    > ```lua
    > default_prog = {'pwsh'},
    > ```

    > 更改 shell 列表：
    >
    > ```lua
    > shellCopy code   table.insert(config.launch_menu, {
    >         label = "Command Prompt",
    >         args = {"cmd.exe"}
    >     })
    >     table.insert(config.launch_menu, {
    >         label = "PowerShell 5",
    >         args = {"powershell.exe", "-NoLogo"}
    >     })
    >     table.insert(config.launch_menu, {
    >         label = "PowerShell 7",
    >         args = {"pwsh.exe", "-NoLogo"}
    >     })
    > 
    >     table.insert(config.launch_menu, {
    >         label = "Anaconda PowerShell Prompt",
    >         args = {"pwsh", "-NoLogo", "-NoExit", "-ExecutionPolicy", "Bypass", "-Command",
    >                 "& 'C:\\ProgramData\\anaconda3\\shell\\condabin\\conda-hook.ps1' ; conda activate 'C:\\ProgramData\\anaconda3' "}
    >     })
    > 
    >     table.insert(config.launch_menu, {
    >         label = "VS Command Prompt 2022 (PowerShell 7)",
    >         args = {"pwsh", "-NoLogo", "-NoExit", "-ExecutionPolicy", "Bypass", "-NoProfile", "-Command",
    >                 " & 'C:\\Program Files\\Microsoft Visual Studio\\2022\\Professional\\Common7\\Tools\\Launch-VsDevShell.ps1'"}
    >     })
    > 
    >     table.insert(config.launch_menu, {
    >         label = "Default WSL Command Prompt",
    >         args = {"wsl"}
    >     })
    > ```

3. 对于中文/英文用户，如果您希望正确获取 `launch_menu`（特别是 wsl 发行版），您应该取消以下行的注释：

```lua
            -- 对于英文用户，默认行：
            -- local distro = line:gsub(" %(Default%)", "")
            -- 对于中文用户，
            local distro = line:gsub(" %(默认%)", "")
```

**您可以在更改配置时更改所有内容。**（如果您有时间阅读 [Wezterm 文档](https://wezfurlong.org/wezterm)。）

> 此存储库没有许可证，您可以随意分发, 请尽情发挥你的创造力。

---

### 后记

> ###### 主题配色
>
> > 原本是我自己写的配置,用的自带的Sukura配色加上自己写的tab栏, 现在的配置文件改为使用[dracula官方提供的配色](https://github.com/dracula/wezterm.git)
> >
> > **原来的**
> >
>> ![img](readme.assets/2283725-20220726143424695-1970924268.png)
> >
>> Dracula**官方提供的配色**
> >
> > ![image-20220810020054548](readme.assets/image-20220810020054548.png)
> >
> > 怎么说,还是Dracula好看!  **Dracula yyds!**
> 
> ###### 关于配置文件
> 
> > 实话的说,我是从一个github的用户Ctrl-CV来的,名字已经忘记了,中间也被我改了一些东西,在此感谢那位不知名的github大佬,也要感谢wezterm带来了如此丰富的自定义终端!

