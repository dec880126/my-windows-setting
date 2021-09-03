# my-windows-setting
整理一下自己習慣用的環境包

## Apps

 - Windows Terminal

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
