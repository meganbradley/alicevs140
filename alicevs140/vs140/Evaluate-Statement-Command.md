---
title: "Evaluate Statement Command"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - vs-ide-general
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 032039bc-9477-4f93-9b9d-66d4be0e90f4
caps.latest.revision: 14
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Evaluate Statement Command
Evaluates and displays the given statement.  
  
## Syntax  
  
```  
Debug.EvaluateStatement text   
```  
  
## Arguments  
 `text`  
 Required. The statement to evaluate.  
  
## Remarks  
 The window used to enter the **EvaluateStatement** command determines whether an equals sign (=) is interpreted as a comparison operator or as an assignment operator.  
  
 In the **Command** window, an equals sign (=) is interpreted as a comparison operator. So, for example, if the values of variables `a` and `b` are different, then the command  
  
```  
>Debug.EvaluateStatement(a=b)  
```  
  
 will return a value of `false`.  
  
 In the **Immediate** window, by contrast, an equals sign (=) is interpreted as an assignment operator. So, for example, the command  
  
```  
>Debug.EvaluateStatement(a=b)  
```  
  
 will assign to variable `a` the value of variable `b`.  
  
## Example  
  
```  
>Debug.EvaluateStatement(a+b)  
```  
  
## See Also  
 [Print Command](../vs140/Print-Command.md)   
 [Visual Studio Commands](../vs140/Visual-Studio-Commands.md)   
 [Command Window](../vs140/Command-Window.md)   
 [Find/Command Box](../vs140/Find-Command-Box.md)   
 [Visual Studio Command Aliases](../vs140/Visual-Studio-Command-Aliases.md)