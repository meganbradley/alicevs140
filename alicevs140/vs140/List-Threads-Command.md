---
title: "List Threads Command"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - vs-ide-general
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 34b665c0-d46f-4c1a-a066-b678eba5ac54
caps.latest.revision: 13
translation.priority.ht: 
  - de-de
  - ja-jp
---
# List Threads Command
Displays a list of the threads in the current program.  
  
## Syntax  
  
```  
Debug.ListThreads [index]  
```  
  
## Arguments  
 `index`  
 Optional. Selects a thread by its index to be the current thread.  
  
## Remarks  
 When specified, the `index` argument marks the indicated thread as the current thread. An asterisk (*) is displayed in the list next to the current thread.  
  
## Example  
  
```  
>Debug.ListThreads   
```  
  
## See Also  
 [List Call Stack Command](../vs140/List-Call-Stack-Command.md)   
 [List Disassembly Command](../vs140/List-Disassembly-Command.md)   
 [Visual Studio Commands](../vs140/Visual-Studio-Commands.md)   
 [Command Window](../vs140/Command-Window.md)   
 [Find/Command Box](../vs140/Find-Command-Box.md)   
 [Visual Studio Command Aliases](../vs140/Visual-Studio-Command-Aliases.md)