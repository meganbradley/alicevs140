---
title: "CPrintDialog::PrintSelection"
ms.custom: na
ms.date: 09/19/2016
ms.devlang: 
  - C++
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - devlang-cpp
ms.tgt_pltfrm: na
ms.topic: reference
ms.assetid: de4e87df-8103-40f3-a42f-6104f336fb12
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CPrintDialog::PrintSelection
Determines whether to print only the currently selected items.  
  
## Syntax  
  
```  
  
BOOL PrintSelection( ) const;  
```  
  
## Return Value  
 Nonzero if only the selected items are to be printed; otherwise 0.  
  
## Remarks  
 Call this function after calling `DoModal` to determine whether to print only the currently selected items.  
  
## Example  
 See the example for [CPrintDialog::m_pd](../vs140/CPrintDialog--m_pd.md).  
  
## Requirements  
 **Header:** afxdlgs.h  
  
## See Also  
 [CPrintDialog Class](../vs140/CPrintDialog-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CPrintDialog::PrintRange](../vs140/CPrintDialog--PrintRange.md)   
 [CPrintDialog::PrintAll](../vs140/CPrintDialog--PrintAll.md)