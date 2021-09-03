# my-windows-setting
整理一下自己習慣用的環境設定

## Apps

 - [Windows Terminal](https://www.microsoft.com/zh-tw/p/windows-terminal/9n0dx20hk701)
 - [Visual Studio Code](https://code.visualstudio.com/)
 - [PowerToys](https://docs.microsoft.com/zh-tw/windows/powertoys/install)
 - [Potplayer](https://potplayer.daum.net/)
 - [WinRAR](https://rar.tw/)
 - [Adobe Acrobat Reader DC](https://get.adobe.com/tw/reader/)
 - [Discord](https://discord.com/download)
 - [Motherboard Drivers](https://tw.msi.com/Motherboard/support/H97-GAMING-3)
 - [VPN(Cisco)](#vpn)

## Oh-my-posh
安裝包
 - 使用系統管理員身分開啟`PowerShell`

`Install-Module posh-git -Scope CurrentUser`<br>
`Install-Module oh-my-posh -Scope CurrentUser`

檢查PROFILE檔，如果沒有就建立

`if (!(Test-Path -Path $PROFILE )) { New-Item -Type File -Path $PROFILE -Force }`

用 `$PROFILE` 檢查 `.ps1` 檔案位置
修改 [Microsoft.PowerShell_profile.ps1](https://github.com/dec880126/my-windows-setting/blob/main/Microsoft.PowerShell_profile.ps1)

## Fonts

### Coding用
 - Fira_Code

### 配合oh-my-posh的符號
 - ShareTechMono

### 中文字體
 - setofont
 - SNsanafonmaruV2

## VS Code 模組

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

## Firefox 設定

1. 網址列輸入`about:config`
2. 將 `media.play-stand-alone` 改成 `false`

## Python

### Downloads
 - [All Releases](https://www.python.org/downloads/)
 - [get-pip.py](https://bootstrap.pypa.io/get-pip.py)

### Pip Modules
`pip install pyinstaller pymysql datetime requests pandas rich bs4 alive-progress tdqm black`

## OS & Office

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
