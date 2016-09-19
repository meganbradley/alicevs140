---
title: "Parameter &#39;&lt;parametername&gt;&#39; in &#39;&lt;methodname&gt;&#39; already has a matching omitted argument"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - devlang-csharp
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: f51d29ba-c5b3-4731-a426-4c5ba11b4e1f
caps.latest.revision: 10
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Parameter &#39;&lt;parametername&gt;&#39; in &#39;&lt;methodname&gt;&#39; already has a matching omitted argument
A procedure call supplies an argument by name after omitting the same argument by position; for example:  
  
```  
Public Sub ABC(ByVal X As Byte, Optional ByVal Y As Byte = 0, _  
                                Optional ByVal Z As Byte = 0)  
' ...  
Call ABC(6, , Y:=3)   ' Argument Y omitted by position, supplied by name.  
```  
  
 **Error ID:** BC32021  
  
### To correct this error  
  
-   Supply the argument by position, or remove the comma that omits it.  
  
## See Also  
 [Passing Arguments by Position and by Name](../vs140/Passing-Arguments-by-Position-and-by-Name--Visual-Basic-.md)