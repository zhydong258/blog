---
title: 'How to delete ms-resource:AppName/Text shortcuts in StartMenu'
date: 2019-09-11 16:52:54
tags: windows
categories: 运维
---
原文出处如下：
“找不到了，反正就是在microsoft的问答上看到的”
引用的原文如下：
For anyone who want to remove ms-resource:AppName/Text, here's a solution:
https://gist.github.com/DoubleLabyrinth/ffae94cb9444bbdae1d11deeaa247310

All you need is this:
Run Powershell with Admin privilege
On the prompt, run this command:
Get-AppxPackage -all *HolographicFirstRun* | Remove-AppPackage -AllUsers
Open Task manager, kill explorer.exe (keep the powershell console open)
Back on the prompt, type:
cd $Env:localappdata\Packages\Microsoft.Windows.StartMenuExperienceHost_cw5n1h2txyewy
If the previous command succesfully put you on AppData\Local\Packages\Microsoft.Windows.StartMenuExperienceHost_cw5n1h2txyewy directory inside your profile dir, then run:
Remove-Item -Recurse -Force .\TempState\
Start explorer.exe back up from task manager (File -> New Task)
The rogue start menu item should be gone.
