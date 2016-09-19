---
title: "CPrintDialog::PrintRange"
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
ms.assetid: ffd0494f-1a43-4de1-a7ea-dce1483039bf
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CPrintDialog::PrintRange
Determines whether to print only a specified range of pages.  
  
## Syntax  
  
```  
  
BOOL PrintRange( ) const;  
```  
  
## Return Value  
 Nonzero if only a range of pages in the document are to be printed; otherwise 0.  
  
## Remarks  
 Call this function after calling `DoModal` to determine whether to print only a range of pages in the document.  
  
## Example  
 See the example for [CPrintDialog::m_pd](../vs140/CPrintDialog--m_pd.md).  
  
## Requirements  
 **Header:** afxdlgs.h  
  
## See Also  
 [CPrintDialog Class](../vs140/CPrintDialog-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CPrintDialog::PrintAll](../vs140/CPrintDialog--PrintAll.md)   
 [CPrintDialog::PrintSelection](../vs140/CPrintDialog--PrintSelection.md)   
 [CPrintDialog::GetFromPage](../vs140/CPrintDialog--GetFromPage.md)   
 [CPrintDialog::GetToPage](../vs140/CPrintDialog--GetToPage.md)