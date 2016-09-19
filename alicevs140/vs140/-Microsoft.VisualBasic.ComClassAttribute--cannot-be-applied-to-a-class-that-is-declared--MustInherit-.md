---
title: "&#39;Microsoft.VisualBasic.ComClassAttribute&#39; cannot be applied to a class that is declared &#39;MustInherit&#39;"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - devlang-csharp
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: c8af606d-f448-4703-98df-e594fd511f92
caps.latest.revision: 10
translation.priority.ht: 
  - de-de
  - ja-jp
---
# &#39;Microsoft.VisualBasic.ComClassAttribute&#39; cannot be applied to a class that is declared &#39;MustInherit&#39;
A class is declared with the <xref:Microsoft.VisualBasic.ComClassAttribute?qualifyHint=False>, but its declaration specifies `MustInherit`.  
  
 To be eligible for COM interop, a .NET Framework class must satisfy the following requirements:  
  
-   It must be `Public`, all its containers must be `Public`, and it must expose at least one `Public` member.  
  
-   It must not be *abstract*, that is, it must not be declared with `MustInherit`.  
  
-   It must not be generic or be declared within a generic container type.  
  
 **Error ID:** BC32508  
  
### To correct this error  
  
-   Remove the `MustInherit` keyword from the class declaration.  
  
     -or-  
  
-   If the class or its containing element must be generic, remove the <xref:Microsoft.VisualBasic.ComClassAttribute?qualifyHint=False> from the class declaration. You cannot expose it to COM.  
  
## See Also  
 <xref:Microsoft.VisualBasic.ComClassAttribute?qualifyHint=False>   
 [COM Interop](../vs140/COM-Interop--Visual-Basic-.md)   
 [MustInherit](../Topic/MustInherit%20\(Visual%20Basic\).md)