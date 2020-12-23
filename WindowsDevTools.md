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
- 默认是`pwsh.exe` 不是 `powershell.exe` 了
```sh
  C:\Users\28268\AppData\Local\Microsoft\WindowsApps\pwsh.exe //IDE我设置的这个路径
  C:\Users\28268\AppData\Local\Microsoft\WindowsApps\Microsoft.PowerShell_8wekyb3d8bbwe\pwsh.exe
  C:\Program Files\WindowsApps\Microsoft.PowerShell_7.1.0.0_x64__8wekyb3d8bbwe\pwsh.exe
```
- 之前装的`posh-git`等都没了
  
## 参考链接
- [比较WSL1 和 WSL2](https://docs.microsoft.com/en-us/windows/wsl/compare-versions)
- [WSL官网文档](https://docs.microsoft.com/zh-cn/windows/wsl/)
- [开发环境文档](https://docs.microsoft.com/zh-cn/windows/dev-environment/overview)
- [powershell-7](https://docs.microsoft.com/zh-cn/powershell/scripting/install/migrating-from-windows-powershell-51-to-powershell-7?view=powershell-7.1)
  