---
title: "CPrintDialog::PrintAll"
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
ms.assetid: a54a8e3f-e891-4a64-83f4-5c460be72604
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CPrintDialog::PrintAll
Determines whether to print all pages of the document.  
  
## Syntax  
  
```  
  
BOOL PrintAll( ) const;  
```  
  
## Return Value  
 Nonzero if all pages in the document are to be printed; otherwise 0.  
  
## Remarks  
 Call this function after calling `DoModal` to determine whether to print all pages in the document.  
  
## Example  
 See the example for [CPrintDialog::m_pd](../vs140/CPrintDialog--m_pd.md).  
  
## Requirements  
 **Header:** afxdlgs.h  
  
## See Also  
 [CPrintDialog Class](../vs140/CPrintDialog-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CPrintDialog::PrintRange](../vs140/CPrintDialog--PrintRange.md)   
 [CPrintDialog::PrintSelection](../vs140/CPrintDialog--PrintSelection.md)