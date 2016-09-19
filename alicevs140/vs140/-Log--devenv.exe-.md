---
title: "-Log (devenv.exe)"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - vs-ide-general
ms.tgt_pltfrm: na
ms.topic: article
H1: /Log (devenv.exe)
ms.assetid: ae23c4ae-2376-4fe3-b8d2-81d34e61c8ba
caps.latest.revision: 10
translation.priority.ht: 
  - de-de
  - ja-jp
---
# -Log (devenv.exe)
Logs all activity to the log file for troubleshooting. This file appears after you've called `devenv /log` at least once. By default, the log file is:  
  
 *%APPDATA%*\Microsoft\VisualStudio\\*Version*\ActivityLog.xml  
  
 where *Version* is the Visual Studio version. However, you may specify a different path and file name.  
  
## Syntax  
  
```  
Devenv /log Path\NameOfLogFile  
```  
  
## Remarks  
 This switch must appear at the end of the command line, after all other switches.  
  
 The log is written for all instances of Visual Studio that you've invoked with the /log switch. It doesn't log instances of Visual Studio that you've invoked without the switch.  
  
## See Also  
 [Devenv Command Line Switches](../vs140/Devenv-Command-Line-Switches.md)