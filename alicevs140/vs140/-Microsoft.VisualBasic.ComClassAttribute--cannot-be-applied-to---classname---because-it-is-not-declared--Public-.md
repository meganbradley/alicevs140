---
title: "&#39;Microsoft.VisualBasic.ComClassAttribute&#39; cannot be applied to &#39;&lt;classname&gt;&#39; because it is not declared &#39;Public&#39;"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - devlang-csharp
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: ac46851f-53ab-4ce6-87b1-4c4d29508527
caps.latest.revision: 10
translation.priority.ht: 
  - de-de
  - ja-jp
---
# &#39;Microsoft.VisualBasic.ComClassAttribute&#39; cannot be applied to &#39;&lt;classname&gt;&#39; because it is not declared &#39;Public&#39;
A class is declared with <xref:Microsoft.VisualBasic.ComClassAttribute?qualifyHint=False>, but its declaration does not specify `Public`.  
  
 To be eligible for COM interop, a .NET Framework class must satisfy the following requirements:  
  
-   It must be `Public`, all its containers must be `Public`, and it must expose at least one `Public` member.  
  
-   It must not be *abstract*, that is, it must not be declared with `MustInherit`.  
  
-   It must not be generic or be declared within a generic container type.  
  
 **Error ID:** BC32509  
  
### To correct this error  
  
-   Add the `Public` keyword to the class declaration.  
  
     -or-  
  
-   If the class or its containing element cannot be `Public`, then remove <xref:Microsoft.VisualBasic.ComClassAttribute?qualifyHint=False> from the class declaration. You cannot expose it to COM.  
  
## See Also  
 <xref:Microsoft.VisualBasic.ComClassAttribute?qualifyHint=False>   
 [COM Interop](../vs140/COM-Interop--Visual-Basic-.md)   
 [Public (Visual Basic)](../vs140/Public--Visual-Basic-.md)