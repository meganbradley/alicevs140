---
title: "CPrintDialog::GetToPage"
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
ms.assetid: b2f12348-73c6-4abd-a32e-f15c533ad997
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CPrintDialog::GetToPage
Retrieves the ending page of the print range.  
  
## Syntax  
  
```  
  
int GetToPage( ) const;  
```  
  
## Return Value  
 The ending page number in the range of pages to be printed.  
  
## Remarks  
 Call this function after calling `DoModal` to retrieve the ending page number in the range of pages to be printed.  
  
## Example  
 See the example for [CPrintDialog::m_pd](../vs140/CPrintDialog--m_pd.md).  
  
## Requirements  
 **Header:** afxdlgs.h  
  
## See Also  
 [CPrintDialog Class](../vs140/CPrintDialog-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CPrintDialog::GetFromPage](../vs140/CPrintDialog--GetFromPage.md)   
 [CPrintDialog::PrintRange](../vs140/CPrintDialog--PrintRange.md)