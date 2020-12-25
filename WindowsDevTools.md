## WSL
- wsl -l  //列出所有子系统
- [win+R] `\\wsl$`  //可视化根目录

- wsl -l -v
- C:\temp> wsl sudo apt-get update
- wsl -s <DistributionName> //设置默认 --setdefault
- wsl npm init //在CMD执行后，在默认WSL运行命令
- wsl --unregister <DistributionName> //取消默认

## PowerShell 7
- 商店下载
- 终端我用的商店下载的 `Terminal`
- 默认是`pwsh.exe` 不是 `powershell.exe` 了
```sh
  C:\Users\28268\AppData\Local\Microsoft\WindowsApps\pwsh.exe //IDE我设置的这个路径
  C:\Users\28268\AppData\Local\Microsoft\WindowsApps\Microsoft.PowerShell_8wekyb3d8bbwe\pwsh.exe
  C:\Program Files\WindowsApps\Microsoft.PowerShell_7.1.0.0_x64__8wekyb3d8bbwe\pwsh.exe
```
- 之前装的`posh-git`等都没了
  
> 安装`posh-git`
```sh
  // or update：PowerShellGet\Update-Module posh-git
  1. PowerShellGet\Install-Module posh-git -Scope CurrentUser -AllowPrerelease -Force
  2. Import-Module posh-git
  3. Add-PoshGitToProfile
```

- notepad $profile.CurrentUserAllHosts //打开了配置文件，不知道写什么`profile.ps1`
```sh
  //查看参考链接
  # Dracula readline configuration. Requires version 2.0, if you have 1.2 convert to `Set-PSReadlineOption -TokenType`
Set-PSReadlineOption -Color @{
    "Command" = [ConsoleColor]::Green
    "Parameter" = [ConsoleColor]::Gray
    "Operator" = [ConsoleColor]::Magenta
    "Variable" = [ConsoleColor]::White
    "String" = [ConsoleColor]::Yellow
    "Number" = [ConsoleColor]::Blue
    "Type" = [ConsoleColor]::Cyan
    "Comment" = [ConsoleColor]::DarkCyan
}
# Dracula Prompt Configuration
Import-Module posh-git
$GitPromptSettings.DefaultPromptPrefix.Text = "$([char]0x2192) " # arrow unicode symbol
$GitPromptSettings.DefaultPromptPrefix.ForegroundColor = [ConsoleColor]::Green
$GitPromptSettings.DefaultPromptPath.ForegroundColor =[ConsoleColor]::Cyan
$GitPromptSettings.DefaultPromptSuffix.Text = "$([char]0x203A) " # chevron unicode symbol
$GitPromptSettings.DefaultPromptSuffix.ForegroundColor = [ConsoleColor]::Magenta
# Dracula Git Status Configuration
$GitPromptSettings.BeforeStatus.ForegroundColor = [ConsoleColor]::Blue
$GitPromptSettings.BranchColor.ForegroundColor = [ConsoleColor]::Blue
$GitPromptSettings.AfterStatus.ForegroundColor = [ConsoleColor]::Blue
```
## 参考链接
- [比较WSL1 和 WSL2](https://docs.microsoft.com/en-us/windows/wsl/compare-versions)
- [WSL官网文档](https://docs.microsoft.com/zh-cn/windows/wsl/)
- [开发环境文档](https://docs.microsoft.com/zh-cn/windows/dev-environment/overview)
- [powershell-7](https://docs.microsoft.com/zh-cn/powershell/scripting/install/migrating-from-windows-powershell-51-to-powershell-7?view=powershell-7.1)
- [posh-git](https://github.com/dahlbyk/posh-git)
- [posh-git-config](https://x-gee-cup.xyz/2020/05/20/powershell%E5%8D%87%E7%BA%A7%E9%85%8D%E8%89%B2/)
  