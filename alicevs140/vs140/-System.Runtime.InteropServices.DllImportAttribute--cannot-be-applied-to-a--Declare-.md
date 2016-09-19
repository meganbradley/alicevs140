---
title: "&#39;System.Runtime.InteropServices.DllImportAttribute&#39; cannot be applied to a &#39;Declare&#39;"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - devlang-csharp
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 04c8a14f-9286-4f9a-aad5-a0555e5f09f4
caps.latest.revision: 10
translation.priority.ht: 
  - de-de
  - ja-jp
---
# &#39;System.Runtime.InteropServices.DllImportAttribute&#39; cannot be applied to a &#39;Declare&#39;
The `DllImportAttribute` attribute was applied to a `Declare` function. This attribute can only be used with an empty `Function` or `Sub`.  
  
 **Error ID:** BC31523  
  
### To correct this error  
  
1.  Remove the `DllImportAttribute` attribute from the `Declare` statement.  
  
## See Also  
 <xref:System.Runtime.InteropServices.DllImportAttribute?qualifyHint=False>   
 [Declare Statement](../Topic/Declare%20Statement.md)