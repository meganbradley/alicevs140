---
title: "&#39;Using&#39; resource variable type can not be array type"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - devlang-csharp
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: f98c54b0-6ede-48b6-aa31-438664c219f3
caps.latest.revision: 12
translation.priority.ht: 
  - de-de
  - ja-jp
---
# &#39;Using&#39; resource variable type can not be array type
A `Using` statement specifies an array variable for a resource.  
  
 The <xref:System.Array?qualifyHint=False> class does not implement the <xref:System.IDisposable?qualifyHint=False> interface, so the `Using` block cannot call the <xref:System.IDisposable.Dispose?qualifyHint=False> method on an array resource.  
  
 **Error ID:** BC36012  
  
### To correct this error  
  
-   Use a different type of system resource in the `Using` block.  
  
## See Also  
 [Using Statement (Visual Basic)](../Topic/Using%20Statement%20\(Visual%20Basic\).md)   
 [How to: Dispose of a System Resource](../Topic/How%20to:%20Dispose%20of%20a%20System%20Resource%20\(Visual%20Basic\).md)   
 [NOTINBUILD Overview of Arrays in Visual Basic](assetId:///ca50e2f2-b4d2-4c57-9169-9abbcc3392d8)