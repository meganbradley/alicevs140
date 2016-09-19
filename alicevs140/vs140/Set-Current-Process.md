---
title: "Set Current Process"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - vs-ide-general
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 1e016ebd-aadd-411f-a606-03bf69d3f8aa
caps.latest.revision: 7
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Set Current Process
Sets the specified process as the active process in the debugger.  
  
## Syntax  
  
```  
Debug.SetCurrentProcess index  
```  
  
## Arguments  
 `index`  
 Required. The index of the process.  
  
## Remarks  
 You can attach to multiple processes when you are debugging, but only one process is active in the dubber at any given time. You can use the `SetCurrentProcess` command to set the active process.  
  
## Example  
  
```  
>Debug.SetCurrentProcess 1  
```  
  
## See Also  
 [Visual Studio Commands](../vs140/Visual-Studio-Commands.md)   
 [Command Window](../vs140/Command-Window.md)   
 [Visual Studio Command Aliases](../vs140/Visual-Studio-Command-Aliases.md)