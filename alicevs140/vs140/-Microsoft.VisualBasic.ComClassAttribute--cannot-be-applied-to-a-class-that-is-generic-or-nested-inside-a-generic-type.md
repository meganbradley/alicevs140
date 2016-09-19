---
title: "&#39;Microsoft.VisualBasic.ComClassAttribute&#39; cannot be applied to a class that is generic or nested inside a generic type"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - devlang-csharp
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: ea125bff-d020-4933-b277-6e24943eea88
caps.latest.revision: 9
translation.priority.ht: 
  - de-de
  - ja-jp
---
# &#39;Microsoft.VisualBasic.ComClassAttribute&#39; cannot be applied to a class that is generic or nested inside a generic type
A class is declared with <xref:Microsoft.VisualBasic.ComClassAttribute?qualifyHint=False>, but it is either generic or contained in a generic class or structure.  
  
 To be eligible for COM interop, a .NET Framework class must satisfy the following requirements:  
  
-   It must be `Public`, all its containers must be `Public`, and it must expose at least one `Public` member.  
  
-   It must not be *abstract*, that is, it must not be declared with `MustInherit`.  
  
-   It must not be generic or be declared within a generic container type.  
  
 **Error ID:** BC31527  
  
### To correct this error  
  
-   Change the declaration of the class so that it is not generic, and make sure its containing element is not generic.  
  
     -or-  
  
-   If the class or its containing element must be generic, remove <xref:Microsoft.VisualBasic.ComClassAttribute?qualifyHint=False> from the class declaration. You cannot expose it to COM.  
  
## See Also  
 <xref:Microsoft.VisualBasic.ComClassAttribute?qualifyHint=False>   
 [COM Interop](../vs140/COM-Interop--Visual-Basic-.md)   
 [Generic Types in Visual Basic](../Topic/Generic%20Types%20in%20Visual%20Basic%20\(Visual%20Basic\).md)