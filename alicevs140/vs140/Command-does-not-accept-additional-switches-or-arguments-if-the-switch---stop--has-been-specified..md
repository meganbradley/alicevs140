---
title: "Command does not accept additional switches or arguments if the switch &quot;-stop&quot; has been specified."
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - devlang-csharp
ms.tgt_pltfrm: na
ms.topic: article
H1: Command does not accept additional switches or arguments if the switch &quot;/stop&quot; has been specified.
ms.assetid: 1dea2450-034e-4a7f-b959-2060811329b6
caps.latest.revision: 9
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Command does not accept additional switches or arguments if the switch &quot;-stop&quot; has been specified.
This error generally occurs when the `/stop` switch has been entered, along with additional switches for the **Find in Files** or **Replace in Files** commands.  
  
### To correct this error  
  
1.  If you want to stop the current Find in Files operation, enter:  
  
    ```  
    Edit.FindinFiles /stop.  
    ```  
  
2.  If you want to stop the current Replace in Files operation, enter:  
  
    ```  
    Edit.ReplaceinFiles /stop  
    ```  
  
3.  If you want to start a new Find in Files or Replace in Files operation, re-enter the command, omitting `/stop`.  
  
## See Also  
 [Replace In Files Command](../vs140/Replace-In-Files-Command.md)   
 [Find in Files Command](../vs140/Find-in-Files-Command.md)   
 [Visual Studio Commands](../vs140/Visual-Studio-Commands.md)