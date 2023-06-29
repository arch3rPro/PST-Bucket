<p align="center">
    <h1 align="center">Scoop Bucket</h1>
</p>
<p align="center">
<b><a href="https://github.com/arch3rPro/PentestTools">PentestTools</a></b>
|
<b><a href="https://github.com/arch3rPro/Pentest-Windows">Pentest-Windows</a></b>
</p>

### SCOOP介绍

Scoop**是一款适用于Windows平台的命令行软件（包）管理工具**。 简单来说，就是可以通过命令行工具（PowerShell、CMD等）实现软件（包）的安装管理等需求，通过简单的一行代码实现软件的下载、安装、卸载、更新等操作。

Scoop bucket **就是一个软件仓库**,本项目旨在服务于项目[Pentest-Windows](https://github.com/arch3rPro/Pentest-Windows)，提供windows渗透测试环境工具进行快捷安装、管理和自动更新。

### scoop基础使用

官网安装说明书： [ScoopInstaller](https://github.com/ScoopInstaller)

1. 先决条件

   - [PowerShell](https://aka.ms/powershell)最新版本或[Windows PowerShell 5.1](https://aka.ms/wmf5download)

2. PowerShell执行策略：

   ```
   Set-ExecutionPolicy -ExecutionPolicy RemoteSigned -Scope CurrentUser
   ```

3. 下载安装脚本,在Powershell中执行以下命令

   ```
   irm get.scoop.sh -outfile 'install.ps1'
   ```

4. 管理员执行安装脚本

   ```
   .\install.ps1 -RunAsAdmin -ScoopDir 'D:\Base\' -ScoopGlobalDir 'D:\Global' -NoProxy
   ```

   其中`-RunAsAdmin`是使用管理员角色执行脚本，`-ScoopDir`指定scoop安装目录，软件默认安装在此。`-ScoopGlobalDir`指定全局程序安装到自定义目录。

5. 安装应用程序

   ```
   scoop install xxxxx -g
   ```

   `xxxx` 为所要安装的软件名称，`-g`指定程序安装到自定义目录，不加`-g`选项则安装到默认目录-g

### 安装该软件仓库中的软件

确保你已经有 Scoop 环境后，执行以下命令订阅本软件仓库：

```powershell
scoop bucket add ar https://github.com/arch3rPro/scoop-bucket
```

执行以下命令安装本仓库中的软件：

```powershell
scoop install ar/<软件名> -g
```

例如

```powershell
scoop install ar/xray -g
scoop install ar/windterm -g
scoop install ar/nuclei -g
scoop install ar/afrog -g
scoop install ar/antsword -g
.......
```

大多数情况下，是可以省略 `ar/`，只需要执行类似 `scoop install nuclei -g` 的命令

### 软件自动更新

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
| scoop install feroxbuster       | 用 Rust 编写的快速、简单、递归的内容发现工具                 | https://github.com/epi052/feroxbuster                        |
| scoop install ffuf              | Fast web fuzzer written in Go                                | <https://github.com/ffuf/ffuf>                               |
| scoop install finalshell        | 国产软件 FinalShell SSH 工具,服务器管理,远程桌面加速软件,支持 Windows,macOS,Linux | <https://www.hostbuf.com/t/988.html>                         |
| scoop install fluentsearch      | 支持工作流的高颜值 Windows 搜索启动器                        | <https://www.fluentsearch.net/>                              |
| scoop install fscan             | 一款内网综合扫描工具，方便一键自动化、全方位漏扫扫描         | https://github.com/shadow1ng/fscan                           |
| scoop install girsh             | Automatically spawn a reverse shell fully interactive for Linux or Windows victim | <https://github.com/nodauf/Girsh>                            |
| scoop install gitrob            | Reconnaissance tool for GitHub organizations                 | <https://github.com/michenriksen/gitrob>                     |
| scoop install goby              | 新一代网络安全技术，通过为目标建立完整的资产数据库，实现快速的安全应急 | https://gobysec.net/                                         |
| scoop install godzilla          | 哥斯拉WebShell管理工具                                       | <https://github.com/BeichenDream/Godzilla>                   |
| scoop install goproxy           | 🔥 Proxy是一个高性能的http代理、https代理、socks5代理、内网穿透代理服务器 | https://github.com/snail007/goproxy/                         |
| scoop install govenom           | Generate MSFVenom shells in command line :)  作者自己写的辣鸡工具 | https://github.com/arch3rPro/Govenom                         |
| scoop install hetty             | An HTTP toolkit for security research.                       | <https://hetty.xyz>                                          |
| scoop install hackbrowserdata   | 一款可全平台运行的浏览器数据导出解密工具                     | https://github.com/moonD4rk/HackBrowserData                  |
| scoop install httpx             | httpx is a fast and multi-purpose HTTP toolkit that allows running multiple probes using the retryablehttp library. It is designed to maintain result reliability with an increased number of threads | <https://projectdiscovery.io>                                |
| scoop install hydra             | 著名的密码爆破工具windows版本                                | <https://github.com/maaaaz/thc-hydra-windows>                |
| scoop install interactsh        | An OOB interaction gathering server and client library       | <https://app.interactsh.com>                                 |
| scoop install jar-analyzer      | 一个用于分析 Jar 包的 GUI 工具，可以用多种方式搜索你想要的信息，自动构建方法调用关系，支持分析 Spring 框架（A Java GUI Tool for Analyzing Jar） | <https://github.com/4ra1n/jar-analyzer>                      |
| scoop install jndinjector       | 一个高度可定制化的 JNDI 和 Java 反序列化利用工具             | <https://github.com/rebeyond/JNDInjector>                    |
| scoop install johnny            | GUI frontend to John the Ripper password cracker             | <https://openwall.info/wiki/john/johnny>                     |
| scoop install john-the-ripper   | John the Ripper jumbo - advanced offline password cracker, which supports hundreds of hash and cipher types, and runs on many operating systems, CPUs, GPUs, and even some FPGAs | <https://www.openwall.com/john/>                             |
| scoop install katana            | A next-generation crawling and spidering framework           | <https://github.com/projectdiscovery/katana>                 |
| scoop install kscan             | Kscan 是一款纯 go 开发的全方位扫描器，具备端口扫描、协议检测、指纹识别，暴力破解等功能。支持协议 1200+，协议指纹 10000+，应用指纹 2000+，暴力破解协议 10 余种。 | <https://github.com/lcvvvv/kscan>                            |
| scoop install ksubdomain        | Subdomain enumeration tool, asynchronous dns packets, use pcap to scan 1600,000 subdomains in 1 second | <https://github.com/boy-hack/ksubdomain>                     |
| scoop install layerdomainfinder | Layer子域名挖掘机是一款域名查询工具，可提供网站子域名查询服务 | <https://github.com/euphrat1ca/LayerDomainFinder>            |
| scoop install masscan           | Mass IP port scanner 快速端口扫描工具                        | https://github.com/robertdavidgraham/masscan                 |
| scoop install mateuszex         | bypass AV生成工具                                            | https://github.com/sairson/MateuszEx                         |
| scoop install maye              | Maye 一个简洁小巧的快速启动工具                              | <https://blog.arae.cc/post/25830.html>                       |
| scoop install mdut              | MDUT - Multiple Database Utilization Tools                   | <https://github.com/SafeGroceryStore/MDUT>                   |
| scoop install  mimikatz         | 一款功能强大的轻量级调试神器,通常用来获取系统账号密码        | https://github.com/gentilkiwi/mimikatz                       |
| scoop install myexploit         | 一款扩展性高的渗透测试框架渗透测试框架端                     | <https://github.com/achuna33/MYExploit>                      |
| scoop install naabu             | projectdiscovery/naabu: A fast port scanner written in go with a focus on reliability and simplicity. Designed to be used in combination with other tools for attack surface discovery in bug bounties and pentests | <https://github.com/projectdiscovery/naabu/>                 |
| scoop install natpass           | 🔥居家办公，远程开发神器                                      | <https://github.com/lwch/natpass>                            |
| scoop install netsparker        | 综合型的web应用安全漏洞扫描工具                              | https://www.invicti.com/                                     |
| scoop install nimscan           | 一款快速端口扫描器                                           | <https://github.com/elddy/NimScan>                           |
| scoop install  nps              | 十分强大的内网穿透代理工具，自带WebUI管理端                  | https://github.com/ehang-io/nps                              |
| scoop install nuclei            | 基于简单的基于 YAML 的 DSL 的快速且可定制的漏洞扫描器        | <https://nuclei.projectdiscovery.io>                         |
| scoop install observerward      | 跨平台社区网页指纹识别工具                                   | <https://0x727.github.io/ObserverWard/>                      |
| scoop install oneforall         | OneForAll是一款功能强大的子域收集工具                        | https://github.com/shmilylty/OneForAll                       |
| scoop install  pagodo           | pagodo (Passive Google Dork) - Automate Google Hacking Database scraping and searching | https://github.com/opsdisk/pagodo                            |
| scoop install peass-ng          | PEASS - 非常牛逼的特权升级查询工具                           | <https://github.com/carlospolop/PEASS-ng>                    |
| scoop install phpenv            | 专业优雅强大的PHP集成环境                                    | https://www.phpenv.cn/                                       |
| scoop install platypus          | 🔨用 go 编写的现代多反向 shell 会话管理器                     | https://github.com/WangYihang/Platypus                       |
| scoop install portforward       | Golang开发的端口转发工具，解决某些场景下内外网无法互通的问题 | https://github.com/knownsec/PortForward                      |
| scoop install postman-cn        | Postman中文版, Complete API development environment          | https://github.com/hlmd/postman-cn                           |
| scoop install PowerRun          | PowerRun (Run with highest privileges) 可以使用 TrustedInstaller/System 的权限来启动一些程序 | <https://www.sordum.org/downloads/?power-run>                |
| scoop install PrintNotifyPotato | 又一个土豆，使用PrintNotify COM服务进行提权                  | https://github.com/BeichenDream/PrintNotifyPotatog           |
| scoop install proguard          | ProGuard, Java optimizer and obfuscator                      | <https://github.com/Guardsquare/proguard>                    |
| scoop install pyxis             | pyxis可以自动识别http和https请求，并获取响应头、状态码、响应大小、响应时间、指纹识别工具（favicon has、service、CMS、framework等） | https://github.com/zan8in/pyxis                              |
| scoop install quake_rs          | Quake搜索引擎-命令行工具                                     | <https://quake.360.cn>                                       |
| scoop install quasar            | Windows远程管理工具-RAT                                      | <https://github.com/quasar/Quasar>                           |
| scoop install rad               | 一款专为安全扫描而生的浏览器爬虫                             | <https://github.com/chaitin/rad>                             |
| scoop install rakshasa          | 基于go编写的跨平台、稳定、隐秘的多级代理内网穿透工具         | https://github.com/Mob2003/rakshasa                          |
| scoop install RegConverter      | Reg Converter is a portable freeware utility to convert .reg data to .bat, .vbs, or .au3. (RegConverter 可以将.reg 文件转换为.bat，.vbs 或.au3。这对于需要管理员权限才能合并到注册表中的文件或无人参与的自动化安装时特别有用。) | <https://www.sordum.org/downloads/?reg-converter>            |
| scoop install reverse_ssh       | 基于SSH的反弹shell工具                                       | https://github.com/NHAS/reverse_ssh                          |
| scoop install rport             | 适用于 Windows、macOS 和 Linux 的自托管开源远程管理解决方案  | https://github.com/realvnc-labs/rport                        |
| scoop install rubick            | 基于 electron 的开源工具箱，自由集成丰富插件（类uTools工具） | https://rubickcenter.github.io/rubick/                       |
| scoop install rustcat           | 现代端口侦听器和反向shell,用Rust编写的类netcat工具           | https://github.com/robiot/rustcat                            |
| scoop install scan4all          | 官方仓库vuls扫描：15000+PoC；23种应用密码破解；7000+网页指标；146个协议和90000+条规则端口扫描；Fuzz, HW,很棒的BugBounty(͡°͜ʖ͡°)... | https://github.com/hktalent/scan4all                         |
| scoop install  scaninfo         | 红队快速漏洞扫描工具                                         | https://github.com/redtoolskobe/scaninfo                     |
| scoop install screentogif       | Screen, webcam and sketchboard recorder with an integrated editor. | <https://www.screentogif.com/>                               |
| scoop install searchdiggity     | Google Hacking Diggity是一个利用搜索引擎（如 Google、Bing）快速识别系统弱点和敏感数据的工具集项目 | https://resources.bishopfox.com/resources/tools/google-hacking-diggity/attack-tools/ |
| scoop install shellcodeloader   | shellcode加载器                                              | https://github.com/knownsec/shellcodeloader                  |
| scoop install skyscorpion       | 基于冰蝎加密流量进行WebShell通信管理客户端                   | <https://github.com/shack2/skyscorpion>                      |
| scoop install sliver            | Adversary Emulation Framework                                | <https://github.com/BishopFox/sliver>                        |
| scoop install  socat            | Socat 是Linux 下的一个多功能的网络工具，此处为非官方的windows版本 | https://github.com/StudioEtrange/socat-windows               |
| scoop install stowaway          | 渗透测试多层网络代理、跳板工具                               | https://github.com/ph4ntonn/Stowaways                        |
| scoop install subfinder         | Subfinder is a subdomain discovery tool that discovers valid subdomains for websites. Designed as a passive framework to be useful for bug bounties and safe for penetration testing | <https://projectdiscovery.io>                                |
| scoop install suo5              | 一款高性能 HTTP 代理隧道工具                                 | A high-performance http proxy tunneling tool                 |
| scoop install super-xray        | XRAY GUI Starter (Web Vulnerability Scanner)                 | <https://github.com/4ra1n/super-xray>                        |
| scoop install termite           | Tool for tunnel (Version 2)                                  | https://github.com/rootkiter/Termite                         |
| scoop install tidefinger        | TideFinger——指纹识别小工具，汲取整合了多个web指纹库，结合了多种指纹检测方法，让指纹检测更快捷、准确 | https://github.com/TideSec/TideFinger                        |
| scoop install transfer          | 集合多个 API 的大文件传输工具                                | <https://github.com/Mikubill/transfer>                       |
| scoop install  txportmap        | 端口扫描、指纹识别工具                                       | https://github.com/4dogs-cn/TXPortMap                        |
| scoop install venom             | 渗透测试多层网络代理、跳板工具                               | https://github.com/Dliv3/Venom                               |
| scoop install verycapture       | 支持长截图，矩形截图，延时截图，任意区域截图，gif 录制，录屏，ocr 翻译等功能 | <https://verycapture.com/cn/download.html>                   |
| scoop install vscan             | 开源、轻量、快速、跨平台 的网站漏洞扫描工具，帮助您快速检测网站安全隐患。功能 端口扫描(port scan) 指纹识别(fingerprint) 漏洞检测(nday check) 智能爆破 (admin brute) 敏感文件扫描(file fuzz) | <https://github.com/veo/vscan>                               |
| scoop install w3cschool         | w3cschool 离线版，包含 HTML,CSS,Javascript,jQuery,C,PHP,Java,Python,Sql,Mysql 等编程语言和开源技术的在线教程及使用手册 | <https://www.w3cschool.cn>                                   |
| scoop install webpathbrute      | 7kbscan-WebPathBrute Web路径暴力探测工具                     | https://github.com/7kbstorm/7kbscan-WebPathBrute             |
| scoop install webshell_generate | 用于生成各类免杀 webshell                                    | <https://github.com/cseroad/Webshell_Generate>               |
| scoop install websocat          | A command-line client for WebSockets, like netcat (or curl) for ws:// with advanced socat-like functions. | https://github.com/vi/websocat                               |
| scoop install windterm          | A professional cross-platform SSH/Sftp/Shell/Telnet/Serial terminal. | <https://github.com/kingToolbox/WindTerm>                    |
| scoop install windynamicdesktop | Port of macOS Mojave Dynamic Desktop feature to Windows 10   | <https://github.com/t1m0thyj/WinDynamicDesktop>              |
| scoop install wub               | wub 彻底关闭 Win10 自动更新工具(Windows Update Blocker)      | <https://www.sordum.org/downloads/?st-windows-update-blocker> |
| scoop install xray              | 一款完善的安全评估工具，支持常见 web 安全问题扫描和自定义 poc | <https://github.com/chaitin/xray>                            |
| scoop install yakit             | 交互式应用安全测试平台，安装成功后需手动启动并初始化本地引擎 | https://github.com/yaklang/yakit                             |
| scoop install ysomap            | Java反序列化利用工具-很棒                                    | <https://github.com/wh1t3p1g/ysomap>                         |
| scoop install yujianportscan    | 一个基于VB.NET + IOCP模型开发的高效端口扫描工具，支持IP区间合并，端口区间合并，端口指纹深度探测。 | <https://github.com/foryujian/yujianportscan>                |
