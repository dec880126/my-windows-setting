# my-windows-setting
整理一下自己常用的Windows環境設定

## Menu
 - [Apps](#apps)
 - [Oh-my-posh](#ohmyposh)
 - [Fonts](#fonts)
 - [VS Code 模組們](#vsModules)
 - [VS Code 設定](#vsSetting)
 - [Firefox 設定](#firefox_setting)
 - [Router 設定](#router)
    - [Archer C80](#archer_c80)
    - [Port Forwarding](#ports)
 - [Python](#python)
     - Pip install
 - [OS & Office](#os_office)
 - [SSH on PowerShell](#ssh_powershell)
 - [Git相關](#git)

<h2 id="apps">Apps</h2>

 - [Windows Terminal](https://www.microsoft.com/zh-tw/p/windows-terminal/9n0dx20hk701)
     - [Oh-my-posh](#ohmyposh)
 - [Visual Studio Code](https://code.visualstudio.com/)
     - [VS Code 模組們](#vsModules)
     - [VS Code 設定](#vsSetting)
 - [PowerToys](https://docs.microsoft.com/zh-tw/windows/powertoys/install)
 - [Potplayer](https://potplayer.daum.net/)
 - [WinRAR](https://rar.tw/)
 - [Adobe Acrobat Reader DC](https://get.adobe.com/tw/reader/)
 - [Discord](https://discord.com/download)
 - [Spotify](https://www.spotify.com/tw/download/windows/)
    - [Spotify黑畫面處理](#solveSpotify)
 - [Motherboard Drivers](https://tw.msi.com/Motherboard/support/H97-GAMING-3)
 - [VPN(Cisco)](#vpn)
 - [Notion](https://www.notion.so/desktop)
 - [Steam](https://store.steampowered.com/about/)
     - [Wallpaper Engine：桌布引擎](https://store.steampowered.com/app/431960/Wallpaper_Engine/)
 - [Garena](https://pc.garena.tw/)
 - [Git 最新版下載](https://git-scm.com/downloads)
 - [Github Windows](https://desktop.github.com/)

<h2 id="ohmyposh">Oh-my-posh</h2>

### 安裝包

 - 使用系統管理員身分開啟`PowerShell`

`Install-Module posh-git -Scope CurrentUser`<br>
`Install-Module oh-my-posh -Scope CurrentUser`

### PROFILE
檢查PROFILE檔，如果沒有就建立

`if (!(Test-Path -Path $PROFILE )) { New-Item -Type File -Path $PROFILE -Force }`

用 `$PROFILE` 檢查 `.ps1` 檔案位置
修改 [Microsoft.PowerShell_profile.ps1](https://github.com/dec880126/my-windows-setting/blob/main/PowerShell/Microsoft.PowerShell_profile.ps1)

### 調整使用者權限
1. 以管理員身分開啟`PowerShell`
2. 輸入指令`Set-ExecutionPolicy RemoteSigned`

<h2 id="fonts">Fonts</h2>

### Coding用
 - Fira_Code

### 配合oh-my-posh的符號
 - MesloLGS NF
 
### 中文字體
 - setofont
 - SNsanafonmaruV2

<h2 id="vsModules">VS Code 模組</h2>

### Tools

 - Power Mode
 - Better Comments
 - Bookmarks
 - Bracket Pair Colorize
 - Markdown ALL in one
 - Markdown Preview Github Styling
 - Todo Tree

### Languages

 - Python
 - Pylance
 - Verilog
 - vscode-drawio
 - C/C++
 - C++ Intellisense

<h2 id="vsSetting">VS Code 設定</h2>

 - Cursor Smooth Caret Animation -> `On`
 - terminal.integrated.fontFamily -> "MesloLGS NF"

已整合於 [.vscode/setting.json](https://github.com/dec880126/my-windows-setting/blob/main/.vscode/settings.json)

<h2 id="firefox_setting">Firefox 設定</h2>

1. 網址列輸入`about:config`
2. 將 `media.play-stand-alone` 改成 `false`

<h2 id="router">Router 設定</h2>

<h3 id="archer_c80"> Archer C80</h3>

 > 為了順利運行L2TP/IPSec VPN server，必須開啟PORT 1701，要安裝這個韌體才可以開啟
 - [TP-LINK BETA版韌體: ArcherC80V121030860033n.bin](https://github.com/dec880126/my-windows-setting/blob/main/Archer_C80/ArcherC80V121030860033n.bin)

1. We here provide a beta firmware for the Archer C80 to allow you to open the 1701 for another server, customers can install it on your C80, then try to open the port 1701 for the local L2TP/IPSec VPN server on the router.

Note:

     1. Please be aware that there is no Onemesh implemented in this beta version, so DON'T install this version if you require to build an Onemesh system with some range extenders.

     2. The router configuration will be restored to the factory defaults, you will need to reconfigure the router settings from scratch.

2. After installing this beta firmware on the Archer C80, please `disable the IPSec Passthrough` on the router. You can find it under `Advanced > Security > ALG` page

<h3 id="ports">Ports</h3>

 - Synology VPN Server (L2TP/IPsec)
    - 1701
    - 500
    - 4500
 - Synology Video Station
    - 9007
 - Synology Web Station
    - 80
    - 443


<h2 id="python">Python</h2>

### Downloads
 - [All Releases](https://www.python.org/downloads/)
 - [get-pip.py](https://bootstrap.pypa.io/get-pip.py)

### Pip Modules
`pip install pyinstaller pymysql datetime requests pandas rich bs4 alive-progress tdqm black openpyxl`

<h2 id="os_office">OS & Office</h2>

 - OS
   - 放在隨身碟(Kingston DataTraveler 100 G3)
 - Office 
   - CyuanMc(NAS) -> /homes/cyuanhuang/PC/ProPlus2019Retail.img

### KMS
- KMS神龍版
- Reloader

<h2 id="vpn">VPN</h2>

1. 次の [URL](https://tus.account.box.com/login?redirect_url=https%3A%2F%2Ftus.app.box.com%2Fs%2F4577m4mvi5pllvr7uqsvdjjsggvcqa0a) にアクセスします。
2. 選擇 `不屬於 東京理科大学`
3. 輸入帳號密碼
4. 下載 `Windows/anyconnect-win-4.10.01075-core-vpn-predeploy-k9.msi`
5. 安裝
6. VPN: Ready to connect. に VPN サーバ名である`tusvpn1.tus.ac.jp`を入力し`Connect`をクリックします
7. 「Username:」と「Password:」の入力域が表示されるので、メールアドレス（学籍番号@ed.tus.ac.jp）とパスワード（CLASSと同一）を入力し「OK」をクリックします。
 - 30分間、無通信状態が続くと自動的に切断されます。その場合、再度手順「①」から行ってください。

<h2 id="solveSpotify">Spotify 黑畫面處理</h2>

1. 打開**Spotify檔案目錄下的locales資料夾**
    - `C:\Users\cyuan\AppData\Roaming\Spotify\locales`
2. 找到`zh-Hant.mo`，並將他改名為`zh-TW.mo`
3. 重新打開 Spotify

<h2 id="ssh_powershell">SSH on PowerShell</h2>

`ssh user@host -p port`

<h2 id = 'git'>Git</h2>

 - [Git 最新版下載](https://git-scm.com/downloads)
 - [Github Windows](https://desktop.github.com/)
