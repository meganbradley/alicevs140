---
title: "&#39;System.Runtime.InteropServices.DllImportAttribute&#39; cannot be applied to a method that is generic or nested in a generic type"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - devlang-csharp
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 6f153808-1945-4c99-85ae-8bd3b35ee5a2
caps.latest.revision: 10
translation.priority.ht: 
  - de-de
  - ja-jp
---
# &#39;System.Runtime.InteropServices.DllImportAttribute&#39; cannot be applied to a method that is generic or nested in a generic type
A procedure is declared with the <xref:System.Runtime.InteropServices.DllImportAttribute?qualifyHint=False>, but either the procedure is generic or it is contained in a generic class or structure.  
  
 The common language runtime (CLR) recognizes this attribute and its <xref:System.Runtime.InteropServices._Assembly.EntryPoint?qualifyHint=False> property as designating a replacement procedure defined in an unmanaged dynamic-link library (DLL) outside the .NET Framework. When code calls the procedure to which the <xref:System.Runtime.InteropServices.DllImportAttribute?qualifyHint=False> is applied, the common language runtime calls the designated unmanaged procedure instead.  
  
 Because unmanaged platforms outside the .NET Framework do not recognize generic types, you cannot interoperate with them using generic types.  
  
 **Error ID:** BC31526  
  
### To correct this error  
  
-   If neither the procedure nor its container needs to be generic, then remove the `Of` clauses so that they are not generic.  
  
-   If the procedure or its container needs to be generic, then remove the <xref:System.Runtime.InteropServices.DllImportAttribute?qualifyHint=False> from the declaration of this procedure.  
  
## See Also  
 <xref:System.Runtime.InteropServices.DllImportAttribute?qualifyHint=False>   
 [Generic Types in Visual Basic](../Topic/Generic%20Types%20in%20Visual%20Basic%20\(Visual%20Basic\).md)