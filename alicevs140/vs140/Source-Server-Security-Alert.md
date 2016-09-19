---
title: "Source Server Security Alert"
ms.custom: na
ms.date: 09/19/2016
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
ms.assetid: 8451c281-6914-469c-b80c-6271cc3f3d17
caps.latest.revision: 10
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Source Server Security Alert
When using Source Server, only use symbol files that are from a known and trusted location.  
  
 This warning appears when you enable Source Server support. Source Server commands are embedded in debug symbol files (PDB files). Make sure you know where your PDB files come from.  
  
> [!IMPORTANT]
>  The following potential security threats must be taken into account when using Source Server: Arbitrary commands can be embedded in the application's PDB file, so make sure you put only the ones you want to execute in the srcsrv.ini file. Any attempt to execute a command not in the srcsvr.ini file will cause a confirmation dialog box to appear. For more information, see [Security Warning: Debugger Must Execute Untrusted Command](../vs140/Security-Warning--Debugger-Must-Execute-Untrusted-Command.md).No validation is done on command parameters, so be careful with trusted commands. For example, if you trusted cmd.exe, a malicious user might specify parameters that would make the command dangerous.  
  
## See Also  
 [Specify Symbol (.pdb) and Source Files in the Visual Studio Debugger](../vs140/Specify-Symbol--.pdb--and-Source-Files-in-the-Visual-Studio-Debugger.md)   
 [Debugger Security](../vs140/Debugger-Security.md)   
 [Source Server](http://msdn.microsoft.com/library/windows/desktop/ms680641.aspx)