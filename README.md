## 简介

本规则基于 [Hackl0us 的 SS-Rule-Snippet 项目](https://github.com/Hackl0us/SS-Rule-Snippet)，并加入了一些适合自己个人的规则片段。本规则不定期随 Hackl0us 的相关规则进行更新

## 导入方法

### ShadowRocket

1. 运行 ShadowRocket，点击下方菜单栏的「配置」，并选择「添加配置」；
2. 在弹出的窗口中，粘贴规则 URL：`https://raw.githubusercontent.com/yyl125/PersonalRules/master/Personal_Shadowrocket_Rules.conf`，点击「下载」按钮；
3. 添加完成后，可在「远程文件」一栏中，看到刚刚粘贴的 URL。单击该 URL，在弹出的菜单中选择「使用配置」；
4. 稍等片刻可以发现「本地文件」一栏中，多出名为 ShadowRocket.conf 的配置文件，左侧有橘色的点，右侧有✅，则表示添加成功

### Clash(X)

Clash 是核心程序，没有图形化界面，但是兼容 Linux / macOS / Windows 三大平台。ClashX 是 Clash 的图形化操作界面版本，内部集成 clash，仅可运行在 macOS 平台。Clash_for_windows_pkg 是 Clash 的图形化操作界面版本，依赖于 Clash 核心程序，二者要处于同一目录下。仅可运行在 Windows 平台。Clash-dashboard 是适配于 Clash 的图形化面板，目前仍在开发，尚未发布。ClashX 1.6.0+ 与 Clash 0.8+ 配置文件可通用。配置文件格式采用 `.yaml`，弃用 `.ini` 格式

两款工具要求配置文件必须存放在 `$HOME/.config/config.yaml`

#### 下载规则

##### 准备工作

Windows 系统请暂时关闭 Windows Defender 的 “实时防护” 功能，否则他可能错误报告威胁，并阻止命令运行。
请确保你的计算机能成功连接到互联网

##### Windows

1. 「开始」-「运行」（或按 Win+R 组合键），输入 cmd 后运行「命令提示符」；
2.  复制并执行以下命令：`mkdir %HOMEPATH%\.config\clash && cd /d %HOMEPATH%\.config\clash && certutil.exe -urlcache -split -f "https://raw.githubusercontent.com/yyl125/PersonalRules/master/Personal_ClashX_Rules.yaml" config.yaml && explorer`；
3. 在弹出的「资源管理器」窗口中，使用文本编辑工具编辑 config.yaml 配置文件即可。

##### macOS

运行 「终端」App；
复制并执行以下命令：`mkdir -p $HOME/.config/clash/ && cd $HOME/.config/clash/ && sudo curl -o ./config.yaml https://raw.githubusercontent.com/yyl125/PersonalRules/master/Personal_ClashX_Rules.yaml -k -s && sudo chmod 775 ./config.yaml && open`；
在弹出的「Finder」窗口中，使用文本编辑工具编辑 config.yaml 配置文件即可

##### Linux

1. 复制并执行以下命令：`mkdir -p $HOME/.config/clash/ && cd $HOME/.config/clash/ && sudo curl -o ./config.yaml https://raw.githubusercontent.com/yyl125/PersonalRules/master/Personal_ClashX_Rules.yaml -k -s && sudo chmod 775 ./config.yaml`；
2. 使用 nano/vim/gedit 等类似工具编辑当前目录下 config.yaml 配置文件即可
