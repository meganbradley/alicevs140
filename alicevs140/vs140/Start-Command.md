---
title: "Start Command"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - vs-ide-general
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: dc4e4aa2-b0ab-4e00-92db-6dc3058ddc21
caps.latest.revision: 15
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Start Command
Begins debugging the startup project.  
  
## Syntax  
  
```  
Debug.Start [address]  
```  
  
## Arguments  
 `address`  
 Optional. The address at which the program suspends execution, similar to a breakpoint in source code. This argument is only valid in debug mode.  
  
## Remarks  
 The **Start** command, when executed, performs a RunToCursor operation to the specified address.  
  
## Example  
 This example starts the debugger and ignores any exceptions that occur.  
  
```  
>Debug.Start  
```  
  
## See Also  
 [Visual Studio Commands](../vs140/Visual-Studio-Commands.md)   
 [Command Window](../vs140/Command-Window.md)   
 [Find/Command Box](../vs140/Find-Command-Box.md)   
 [Visual Studio Command Aliases](../vs140/Visual-Studio-Command-Aliases.md)