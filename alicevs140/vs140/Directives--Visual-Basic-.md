---
title: "Directives (Visual Basic)"
ms.custom: na
ms.date: 09/19/2016
ms.devlang: 
  - VB
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - devlang-visual-basic
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 20d5fe65-490a-4c23-88c2-ee4f490ed762
caps.latest.revision: 11
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Directives (Visual Basic)
The topics in this section document the Visual Basic source code compiler directives.  
  
## In This Section  
 [#Const Directive](../vs140/#Const-Directive.md) -- Define a compiler constant  
  
 [#ExternalSource Directive](../vs140/#ExternalSource-Directive.md) -- Indicate a mapping between source lines and text external to the source  
  
 [#If...Then...#Else Directives](../vs140/#If...Then...#Else-Directives.md) -- Compile selected blocks of code  
  
 [#Region Directive](../vs140/#Region-Directive.md) -- Collapse and hide sections of code in the Visual Studio editor  
  
 **#Disable, #Enable** -- Disable and enable specific warnings for regions of code.  
  
```vb  
#Disable Warning BC42356 ' suppress warning about no awaits in this method  
    Async Function TestAsync() As Task  
        Console.WriteLine("testing")  
    End Function  
#Enable Warning BC42356  
  
```  
  
 You can disable and enable a comma-separated list of warning codes too.  
  
## Related Sections  
 [Visual Basic Language Reference](../Topic/Visual%20Basic%20Language%20Reference.md)  
  
 [Visual Basic](../vs140/Visual-Basic.md)