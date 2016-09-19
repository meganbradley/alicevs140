---
title: "&#39;Using&#39; operand of type &#39;&lt;typename&gt;&#39; must implement System.IDisposable"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - devlang-csharp
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: ae9ed5d5-68ba-4950-bb7a-61327fa0e7d5
caps.latest.revision: 10
translation.priority.ht: 
  - de-de
  - ja-jp
---
# &#39;Using&#39; operand of type &#39;&lt;typename&gt;&#39; must implement System.IDisposable
A `Using` statement specifies a resource of a type that does not implement the <xref:System.IDisposable?qualifyHint=False> interface.  
  
 The purpose of a `Using` block is to guarantee the disposal of a system resource when exiting the block. To satisfy this purpose, the resource must expose the <xref:System.IDisposable.Dispose?qualifyHint=False> method implemented from <xref:System.IDisposable?qualifyHint=False>.  
  
 **Error ID:** BC36010  
  
### To correct this error  
  
-   Remove the resource from the resource list of the `Using` statement, or replace it with a resource that implements <xref:System.IDisposable?qualifyHint=False>.  
  
## See Also  
 <xref:System.IDisposable?qualifyHint=False>   
 [Using Statement (Visual Basic)](../Topic/Using%20Statement%20\(Visual%20Basic\).md)   
 [How to: Dispose of a System Resource](../Topic/How%20to:%20Dispose%20of%20a%20System%20Resource%20\(Visual%20Basic\).md)