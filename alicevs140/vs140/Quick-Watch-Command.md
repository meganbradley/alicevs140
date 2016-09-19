---
title: "Quick Watch Command"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - vs-ide-general
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 9670ac3a-8f2f-4874-974d-cb87d3b0cde1
caps.latest.revision: 13
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Quick Watch Command
Displays the selected or specified text in the Expression field of the [QuickWatch Dialog Box](../vs140/How-to--Use-the-QuickWatch-Dialog-Box.md). You can use this dialog box to calculate the current value of a variable or expression recognized by the debugger, or the contents of a register. In addition, you can change the value of any non-const variable or the contents of any register.  
  
## Syntax  
  
```  
Debug.QuickWatchq [text]  
```  
  
## Arguments  
 `text`  
 Optional. The text to add to the **QuickWatch** dialog box.  
  
## Remarks  
 If `text` is omitted, the currently selected text or word at the cursor is added to the Watch window.  
  
## Example  
  
```  
>Debug.QuickWatch  
```  
  
## See Also  
 [How to: Use the QuickWatch Dialog Box](../vs140/How-to--Use-the-QuickWatch-Dialog-Box.md)   
 [Visual Studio Commands](../vs140/Visual-Studio-Commands.md)   
 [Command Window](../vs140/Command-Window.md)   
 [Find/Command Box](../vs140/Find-Command-Box.md)   
 [Visual Studio Command Aliases](../vs140/Visual-Studio-Command-Aliases.md)