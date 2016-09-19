---
title: "&#39;For Each&#39; on type &#39;&lt;typename&gt;&#39; is ambiguous because the type implements multiple instantiations of &#39;System.Collections.Generic.IEnumerable(Of T)&#39;"
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
ms.assetid: ed20d09c-913f-482e-89f8-c0a596c3ec24
caps.latest.revision: 9
translation.priority.ht: 
  - de-de
  - ja-jp
---
# &#39;For Each&#39; on type &#39;&lt;typename&gt;&#39; is ambiguous because the type implements multiple instantiations of &#39;System.Collections.Generic.IEnumerable(Of T)&#39;
A `For Each` statement specifies an iterator variable that has more than one <xref:System.Collections.IEnumerable.GetEnumerator?qualifyHint=False> method.  
  
 The iterator variable must be of a type that implements the <xref:System.Collections.IEnumerable?qualifyHint=True> or <xref:System.Collections.Generic.IEnumerable`1?qualifyHint=True> interface in one of the `Collections` namespaces of the [!INCLUDE[dnprdnshort](../vs140/includes/dnprdnshort_md.md)]. It is possible for a class to implement more than one constructed generic interface, using a different type argument for each construction. If a class that does this is used for the iterator variable, that variable has more than one <xref:System.Collections.IEnumerable.GetEnumerator?qualifyHint=False> method. In such a case, [!INCLUDE[vbprvb](../vs140/includes/vbprvb_md.md)] cannot choose which method to call.  
  
 **Error ID:** BC32096  
  
### To correct this error  
  
-   Use [DirectCast](../Topic/DirectCast%20Operator%20\(Visual%20Basic\).md) or [TryCast](../Topic/TryCast%20Operator%20\(Visual%20Basic\).md) to cast the iterator variable type to the interface defining the <xref:System.Collections.IEnumerable.GetEnumerator?qualifyHint=False> method you want to use.  
  
## See Also  
 [For Each...Next Statement (Visual Basic)](../Topic/For%20Each...Next%20Statement%20\(Visual%20Basic\).md)   
 [Interfaces (Visual Basic)](../vs140/Interfaces--Visual-Basic-.md)