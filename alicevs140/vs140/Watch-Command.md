---
title: "Watch Command"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - vs-ide-general
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: aa02e647-d9f5-4905-a651-52a8df595795
caps.latest.revision: 13
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Watch Command
Creates and opens a specified instance of a **Watch** window. You can use a **Watch** window to calculate the values of variables, expressions, and registers, to edit these values, and to save the results.  
  
## Syntax  
  
```  
Debug.Watch[index]  
```  
  
## Arguments  
 `index`  
 Required. The instance number of the watch window.  
  
## Remarks  
 The `index` must be an integer. Valid values are 1, 2, 3, or 4.  
  
## Example  
  
```  
>Debug.Watch1  
```  
  
## See Also  
 [How to: Use Debugger Variable Windows](../vs140/Autos-and-Locals-Windows.md)   
 [How to: Edit a Value in the Watch Window](../vs140/How-to--Edit-a-Value-in-a-Variable-Window.md)   
 [How to: Use the QuickWatch Dialog Box](../vs140/How-to--Use-the-QuickWatch-Dialog-Box.md)   
 [Visual Studio Commands](../vs140/Visual-Studio-Commands.md)   
 [Command Window](../vs140/Command-Window.md)   
 [Find/Command Box](../vs140/Find-Command-Box.md)   
 [Visual Studio Command Aliases](../vs140/Visual-Studio-Command-Aliases.md)