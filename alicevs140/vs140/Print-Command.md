---
title: "Print Command"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - vs-ide-general
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 0412d381-590a-483f-bab4-6e1cca095645
caps.latest.revision: 12
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Print Command
Evaluates an expression, or displays specified text.  
  
## Syntax  
  
```  
Debug.Print text  
```  
  
## Arguments  
 `text`  
 Required. The expression to evaluate or the text to display.  
  
## Remarks  
 You can use the question mark (?) as an alias for this command. So, for example, the command  
  
```  
>Debug.Print expA  
```  
  
 can also be written  
  
```  
>? expA  
```  
  
 Both versions of this command will return the current value of the expression `expA`.  
  
## Example  
  
```  
>Debug.Print varA  
```  
  
## See Also  
 [Evaluate Statement Command](../vs140/Evaluate-Statement-Command.md)   
 [Visual Studio Commands](../vs140/Visual-Studio-Commands.md)   
 [Command Window](../vs140/Command-Window.md)   
 [Find/Command Box](../vs140/Find-Command-Box.md)   
 [Visual Studio Command Aliases](../vs140/Visual-Studio-Command-Aliases.md)