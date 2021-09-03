# my-windows-setting
整理一下自己習慣用的環境設定

## Apps

 - [Windows Terminal](https://www.microsoft.com/zh-tw/p/windows-terminal/9n0dx20hk701)
 - [Visual Studio Code](https://code.visualstudio.com/)
 - [PowerToys](https://docs.microsoft.com/zh-tw/windows/powertoys/install)

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

`pip install pyinstaller pymysql datetime requests pandas rich bs4 alive-progress tdqm black`
