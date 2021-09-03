# my-windows-setting
整理一下自己習慣用的環境包

## Apps

 - Windows Terminal

## Oh-my-posh
安裝包

`Install-Module posh-git -Scope CurrentUser`
`Install-Module oh-my-posh -Scope CurrentUser`

檢查PROFILE檔，如果沒有就建立

`if (!(Test-Path -Path $PROFILE )) { New-Item -Type File -Path $PROFILE -Force }`

用 `$PROFILE` 檢查 `.ps1` 檔案位置
修改 Microsoft.PowerShell_profile.ps1
