---
title: Abp vNext debug
date: 2020-05-23 17:42:02
tags:
    - Abp
categories:
  - Frontend
---

> Abp supports SourceLink
> 
> ![image](https://user-images.githubusercontent.com/6908465/56625111-5af5ba80-666e-11e9-9238-ff3714403c06.png)
>
> https://github.com/abpframework/abp/issues/1039
> https://aspnetboilerplate.com/Pages/Documents/Debugging


I set as mentioned above, it doesn't work. 
You should do more settings:
1. Enable Symbol Serves
![image](https://user-images.githubusercontent.com/6952917/77402653-f39a3a80-6de9-11ea-8cce-d06a0f62376d.png)

After this, you can debug the asp.net core source code, you can see the  Symbols loaded in output window, but volo.abo.* symbols cannot be loaded. I don't know why?
![image](https://user-images.githubusercontent.com/6952917/77403594-61933180-6deb-11ea-8cbe-43f40b5a70ea.png)

2.Copy Volo.Abp.Core.dll and Volo.Abp.Core.pdb to your working debug bin folder.
There are in the nuget install package path, like "C:\Users\[your user name]\\.nuget\packages\volo.abp.core\2.3.0\lib\netstandard2.0"

After this I can step into abp source code, see my screenshots:
![image](https://user-images.githubusercontent.com/6952917/77403635-740d6b00-6deb-11ea-83a4-c84fd105e017.png)

![image](https://user-images.githubusercontent.com/6952917/77402461-ad44db80-6de9-11ea-9338-81b9762b7f94.png)
![image](https://user-images.githubusercontent.com/6952917/77402491-b635ad00-6de9-11ea-9e46-8539b1429758.png)

>More detail: https://www.cnblogs.com/GerryGe/