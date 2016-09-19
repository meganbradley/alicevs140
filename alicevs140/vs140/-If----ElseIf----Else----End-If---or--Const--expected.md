---
title: "&#39;If&#39;, &#39;ElseIf&#39;, &#39;Else&#39;, &#39;End If&#39;, or &#39;Const&#39; expected"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - devlang-csharp
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: fa3bf591-8036-459c-8c29-ed7784e444f6
caps.latest.revision: 12
translation.priority.ht: 
  - de-de
  - ja-jp
---
# &#39;If&#39;, &#39;ElseIf&#39;, &#39;Else&#39;, &#39;End If&#39;, or &#39;Const&#39; expected
A source line begins with a `#` character, but a valid conditional compilation directive does not immediately follow the `#`. Valid directives include `#Const`, `#ExternalSource`, `#If`, `#Else`, `#ElseIf`, `#End If`, and `#Region`.  
  
 **Error ID:** BC30248  
  
### To correct this error  
  
1.  Make sure the conditional compilation directive is spelled correctly.  
  
2.  Make sure there is no intervening space between the `#` character and the directive.  
  
3.  Remove the `#` character or add a valid directive immediately after it.  
  
## See Also  
 [Directives](../vs140/Directives--Visual-Basic-.md)