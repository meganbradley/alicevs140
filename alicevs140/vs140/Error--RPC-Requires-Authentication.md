---
title: "Error: RPC Requires Authentication"
ms.custom: na
ms.date: 09/18/2016
ms.devlang: 
  - FSharp
  - VB
  - CSharp
  - C++
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - vs-ide-debug
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 88362b3b-8fbe-431f-96a4-80e2d822bbc7
caps.latest.revision: 13
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Error: RPC Requires Authentication
The Visual Studio debugger cannot connect to the remote computer. An RPC policy is enabled on the local computer which prevents remote debugging.  
  
### To correct this error  
  
1.  Run `\`*windir*`\system32\regedt32.exe`  
  
2.  Locate and delete `HKEY_LOCAL_MACHINE\Software\Policies\Microsoft\Windows NT\RPC\RestrictRemoteClients`.  
  
3.  Restart your computer so the registry change will take effect.  
  
4.  If the problem persists, contact your domain administrator about the **Computer Configuration->Administrative Templates->System->Remote Procedure Call->Restrictions for Unauthenticated RPC clients** group policy setting.