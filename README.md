# scoop bucket

## 安装 scoop

---

如果不明白 scoop 是什么，点击查看这里 [scoop](https://github.com/ScoopInstaller/Scoop)

可以简单理解为 scoop 是一个绿色软件的自动安装管理工具

## 安装该软件仓库中的软件

---

确保你已经有 Scoop 环境后，执行以下命令订阅本软件仓库：

```powershell
scoop bucket add ar https://github.com/arch3rPro/scoop-bucket
```

执行以下命令安装本仓库中的软件：

```powershell
scoop install ar/<软件名> |
```

例如

```powershell
scoop install ar/xray
scoop install ar/windterm
scoop install ar/nuclei
scoop install ar/afrog
scoop install ar/antsword
.......
```

大多数情况下，是可以省略 `ar/`，只需要执行类似 `scoop install nuclei` 的命令

## 软件自动更新

---

这个仓库已经添加 github ci 自动化，每隔几个小时会自动更新所有软件到最新版本

使用者可以自行在系统中加个定时任务，这样就能自动更新 scoop 软件了，当然也可以手工更新

```powershell
scoop update *
```

单个软件的更新可以使用下列命令，大多数情况下软件名不重复的话，可以省略 `ar/`，只需要执行类似 `scoop update xray` 的命令

```powershell
scoop update ar/xray
scoop update ar/windterm
scoop update ar/screentogif
.......
```

## 现有适配软件

---

| **关注持续更新, 有问题提 issue**

---

| 软件                            | 描述                                                         | 官网地址                                                     |
| :------------------------------ | :----------------------------------------------------------- | :----------------------------------------------------------- |
| scoop install afrog             | afrog 是一款性能卓越、快速稳定、PoC 可定制化的漏洞扫描工具 - A tool for finding vulnerabilities | <https://github.com/zan8in/afrog>                            |
| scoop install antsword          | 中国蚁剑加载器，安装完成后需要初始化                         | https://github.com/AntSwordProject/AntSword-Loader           |
| scoop install av_evasion_tool   | 掩日 - 免杀执行器生成工具                                    | https://github.com/1y0n/AV_Evasion_Tool                      |
| scoop install bantam            | A PHP backdoor management and generation tool/C2 featuring end to end encrypted payload streaming designed to bypass WAF, IDS, SIEM systems.s | https://github.com/gellin/bantam                             |
| scoop install behinder          | “冰蝎”动态二进制加密网站管理客户端                           | https://github.com/rebeyond/Behinder                         |
| scoop install beroot            | 本地提权辅助工具 - Privilege Escalation Project - Windows / Linux / Mac | <https://github.com/AlessandroZ/BeRoot>                      |
| scoop install broxy             | GO编写的HTTP协议代理抓包工具 -An HTTP/HTTPS intercept proxy written in Go. | <https://github.com/rhaidiz/broxy>                           |
| scoop install burpsuite         | Burpsuite 吾爱破解版，需自行检测后门，安装后需注册           | https://www.52pojie.cn/thread-1544866-1-1.html               |
| scoop install burpsuite-np      | Burpsuite 官方版，安装后需注册                               | https://portswigger.net/                                     |
| scoop install cobaltstrike      | cobaltstrike 雨苁大佬版                                      | <https://www.ddosi.org/?s=cobalt+strike>                     |
| scoop install ct                | ct 是一款性简单易用的域名爆破工具                            | <https://github.com/knownsec/ct>                             |
| scoop install dalfox            | 🌙🦊 Dalfox is a powerful open-source XSS scanner and utility focused on automation. | https://github.com/hahwul/dalfox                             |
| scoop install DeimosC2          | DeimosC2 is a Golang command and control framework for post-exploitation. | <https://github.com/DeimosC2/DeimosC2>                       |
| scoop install dig               | dig (domain information groper) is a flexible tool for interrogating DNS name servers | <https://www.isc.org/bind/>                                  |
| scoop install dirbuster         | DirBuster是一个多线程的基于Java的应用程序设计用于暴力破解Web 应用服务器上的目录名和文件名的工具 | <https://sourceforge.net/projects/dirbuster/>                |
| scoop install dnsx              | A fast and multi-purpose DNS toolkit allow to run multiple DNS queries | <https://github.com/projectdiscovery/dnsx>                   |
| scoop install ehole             | EHole(棱洞)3.0 重构版-红队重点攻击系统指纹探测工具           | https://github.com/EdgeSecurityTeam/EHole                    |
| scoop install ffuf              | Fast web fuzzer written in Go                                | <https://github.com/ffuf/ffuf>                               |
| scoop install finalshell        | 国产软件 FinalShell SSH 工具,服务器管理,远程桌面加速软件,支持 Windows,macOS,Linux | <https://www.hostbuf.com/t/988.html>                         |
| scoop install dev-sidecar       | 开发者边车，github 打不开，github 加速，git clone 加速，git release 下载加速，stackoverflow 加速 . | <https://github.com/docmirror/dev-sidecar>                   |
| scoop install easy-context-menu | Easy Context Menu (ECM) lets you add a variety of useful commands and tweaks to the Desktop, My Computer, Drives, File and Folder right-click context menus. This enables you to access the most used Windows components quickly and easily. Simply check the box next to the items you wish to add. Once added, just right click and the select the component shortcut to launch it. Easy Context Menu is both portable and freeware. | <https://www.sordum.org/7615/>                               |
| scoop install edx               | 一款高性能的可扩展编辑器                                     | <https://www.ed-x.cc/index.html>                             |
| scoop install emeditor          | EmEditor is a fast, lightweight, yet extensible, easy-to-use text editor for Windows. | <https://www.emeditor.com/>                                  |
| scoop install extremedumper     | .NET Assembly Dumper                                         | <https://github.com/wwh1004/ExtremeDumper>                   |
| scoop install fab               | Firewall App Blocker (Fab) 易于使用的 Windows 防火墙工具     | <https://www.sordum.org/downloads/?firewall-app-blocker>     |
| scoop install fastgithub        | github 加速神器，解决 github 打不开、用户头像无法加载、releases 无法上传下载、git-clone、git-pull、git-push 失败等问题. | <https://github.com/dotnetcore/FastGithub>                   |
| scoop install gda               | the fastest and most powerful android decompiler(native tool working without Java VM) for the APK, DEX, ODEX, OAT, JAR, AAR, and CLASS file. which supports malicious behavior detection, privacy leaking detection, vulnerability detection, path solving, packer identification, variable tracking, deobfuscation, python&java scripts, device memory extraction, data decryption, and encryption, etc | <https://github.com/charles2gan/GDA-android-reversing-Tool>  |
| scoop install git-repo-clean    | 对 Git 仓库大文件进行扫描、清理，并重写提交历史的 Git 拓展工具。 | <https://gitee.com/oschina/git-repo-clean>                   |
| scoop install godzilla          | 哥斯拉                                                       | <https://github.com/BeichenDream/Godzilla>                   |
| scoop install httpx             | httpx is a fast and multi-purpose HTTP toolkit that allows running multiple probes using the retryablehttp library. It is designed to maintain result reliability with an increased number of threads | <https://projectdiscovery.io>                                |
| scoop install igdm              | Desktop application for Instagram DMs                        | <https://github.com/igdmapps/igdm/>                          |
| scoop install interactsh        | An OOB interaction gathering server and client library       | <https://app.interactsh.com>                                 |
| scoop install jar-analyzer      | 一个用于分析 Jar 包的 GUI 工具，可以用多种方式搜索你想要的信息，自动构建方法调用关系，支持分析 Spring 框架（A Java GUI Tool for Analyzing Jar） | <https://github.com/4ra1n/jar-analyzer>                      |
| scoop install jndinjector       | 一个高度可定制化的 JNDI 和 Java 反序列化利用工具             | <https://github.com/rebeyond/JNDInjector>                    |
| scoop install katana            | A next-generation crawling and spidering framework           | <https://github.com/projectdiscovery/katana>                 |
| scoop install kscan             | Kscan 是一款纯 go 开发的全方位扫描器，具备端口扫描、协议检测、指纹识别，暴力破解等功能。支持协议 1200+，协议指纹 10000+，应用指纹 2000+，暴力破解协议 10 余种。 | <https://github.com/lcvvvv/kscan>                            |
| scoop install ksubdomain        | Subdomain enumeration tool, asynchronous dns packets, use pcap to scan 1600,000 subdomains in 1 second | <https://github.com/boy-hack/ksubdomain>                     |
| scoop install maye              | Maye 一个简洁小巧的快速启动工具                              | <https://blog.arae.cc/post/25830.html>                       |
| scoop install mdut              | MDUT - Multiple Database Utilization Tools                   | <https://github.com/SafeGroceryStore/MDUT>                   |
| scoop install MonitorOff        | MonitorOff (Screen Turns Off)                                | <https://www.sordum.org/downloads/?st-sordum-monitor-off>    |
| scoop install naabu             | projectdiscovery/naabu: A fast port scanner written in go with a focus on reliability and simplicity. Designed to be used in combination with other tools for attack surface discovery in bug bounties and pentests | <https://github.com/projectdiscovery/naabu/>                 |
| scoop install newfiletime       | NewFileTime is a Windows tool that provides you easy access to correct or manipulate any of the timestamps for any file and folder on Windows! | <http://www.softwareok.com/?seite=Microsoft/NewFileTime>     |
| scoop install notepad--         | 一个支持 windows/linux/mac 的文本编辑器，目标是要替换 notepad++，来自中国。 | <https://github.com/cxasm/notepad-->                         |
| scoop install notify            | Notify is a Go-based assistance package that enables you to stream the output of several tools (or read from a file) and publish it to a variety of supported platforms | <https://projectdiscovery.io>                                |
| scoop install nuclei            | Fast and customizable vulnerability scanner based on simple YAML based DSL | <https://nuclei.projectdiscovery.io>                         |
| scoop install observerward      | Cross platform community web fingerprint identification tool | <https://0x727.github.io/ObserverWard/>                      |
| scoop install postman-cn        | Postman 中文版, Complete API development environment.        | <https://github.com/hlmd/postman-cn>                         |
| scoop install PowerRun          | PowerRun (Run with highest privileges) 可以使用 TrustedInstaller/System 的权限来启动一些程序 | <https://www.sordum.org/downloads/?power-run>                |
| scoop install proguard          | ProGuard, Java optimizer and obfuscator                      | <https://github.com/Guardsquare/proguard>                    |
| scoop install quake_rs          | Quake Command-Line Application                               | <https://quake.360.cn>                                       |
| scoop install quasar            | Remote Administration Tool for Windows                       | <https://github.com/quasar/Quasar>                           |
| scoop install rad               | 一款专为安全扫描而生的浏览器爬虫                             | <https://github.com/chaitin/rad>                             |
| scoop install RegConverter      | Reg Converter is a portable freeware utility to convert .reg data to .bat, .vbs, or .au3. (RegConverter 可以将.reg 文件转换为.bat，.vbs 或.au3。这对于需要管理员权限才能合并到注册表中的文件或无人参与的自动化安装时特别有用。) | <https://www.sordum.org/downloads/?reg-converter>            |
| scoop install scan4all          | Official repository vuls Scan: 15000+PoCs; 23 kinds of application password crack; 7000+Web fingerprints; 146 protocols and 90000+ rules Port scanning; Fuzz, HW, awesome BugBounty( ͡° ͜ʖ ͡°).. | <https://scan4all.51pwn.com>                                 |
| scoop install screentogif       | Screen, webcam and sketchboard recorder with an integrated editor. | <https://www.screentogif.com/>                               |
| scoop install siyuan            | SiYuan is a local-first personal knowledge management system, support fine-grained block-level reference and Markdown instant-render editing. | <https://github.com/siyuan-note/siyuan>                      |
| scoop install sliver            | Adversary Emulation Framework                                | <https://github.com/BishopFox/sliver>                        |
| scoop install subfinder         | Subfinder is a subdomain discovery tool that discovers valid subdomains for websites. Designed as a passive framework to be useful for bug bounties and safe for penetration testing | <https://projectdiscovery.io>                                |
| scoop install super-xray        | XRAY GUI Starter (Web Vulnerability Scanner)                 | <https://github.com/4ra1n/super-xray>                        |
| scoop install transfer          | 集合多个 API 的大文件传输工具                                | <https://github.com/Mikubill/transfer>                       |
| scoop install treesize          | TreeSize 纯净版是一款功能强大的磁盘空间管理软件，为用户提供了功能强大的磁盘空间管理功能，帮助更好的管理内存空间，为文件管理提供了帮助。软件已经进行了整体优化，去除了各种无用的功能和界面，满足用户的各种软件纯净版使用需求 | <https://www.jam-software.com/treesize>                      |
| scoop install verycapture       | 支持长截图，矩形截图，延时截图，任意区域截图，gif 录制，录屏，ocr 翻译等功能 | <https://verycapture.com/cn/download.html>                   |
| scoop install vscan             | 开源、轻量、快速、跨平台 的网站漏洞扫描工具，帮助您快速检测网站安全隐患。功能 端口扫描(port scan) 指纹识别(fingerprint) 漏洞检测(nday check) 智能爆破 (admin brute) 敏感文件扫描(file fuzz) | <https://github.com/veo/vscan>                               |
| scoop install w3cschool         | w3cschool 离线版，包含 HTML,CSS,Javascript,jQuery,C,PHP,Java,Python,Sql,Mysql 等编程语言和开源技术的在线教程及使用手册 | <https://www.w3cschool.cn>                                   |
| scoop install webshell_generate | 用于生成各类免杀 webshell                                    | <https://github.com/cseroad/Webshell_Generate>               |
| scoop install windterm          | A professional cross-platform SSH/Sftp/Shell/Telnet/Serial terminal. | <https://github.com/kingToolbox/WindTerm>                    |
| scoop install windynamicdesktop | Port of macOS Mojave Dynamic Desktop feature to Windows 10   | <https://github.com/t1m0thyj/WinDynamicDesktop>              |
| scoop install wub               | wub 彻底关闭 Win10 自动更新工具(Windows Update Blocker)      | <https://www.sordum.org/downloads/?st-windows-update-blocker> |
| scoop install xray              | 一款完善的安全评估工具，支持常见 web 安全问题扫描和自定义 poc | <https://github.com/chaitin/xray>                            |
| scoop install anew              | A tool for adding new lines to files, skipping duplicates    | <https://github.com/tomnomnom/anew>                          |
| scoop install gowitness         | gowitness - a golang, web screenshot utility using Chrome Headless | <https://github.com/sensepost/gowitness>                     |
| scoop install suo5              | 一款高性能 HTTP 代理隧道工具                                 | A high-performance http proxy tunneling tool                 |
| scoop install rubick            | Electron based open source toolbox, free integration of rich plug-ins. 基于 electron 的开源工具箱，自由集成丰富插件。 | <https://rubickcenter.github.io/rubick/>                     |
| scoop install pyxis             | pyxis can automatically identify http and https requests, and get response headers, status codes, response size, response time, tools for fingerprinting (favicon has, service, CMS, framework, etc.) | <https://github.com/zan8in/pyxis>                            |
| scoop install rakshasa          | 基于go编写的跨平台、稳定、隐秘的多级代理内网穿透工具         | <https://github.com/Mob2003/rakshasa>                        |
