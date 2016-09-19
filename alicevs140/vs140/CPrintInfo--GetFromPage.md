---
title: "CPrintInfo::GetFromPage"
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
ms.assetid: c068bfc4-1b99-4504-ad50-d3eecae52eb0
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CPrintInfo::GetFromPage
Call this function to retrieve the number of the first page to be printed.  
  
## Syntax  
  
```  
  
UINT GetFromPage( ) const;  
```  
  
## Return Value  
 The number of the first page to be printed.  
  
## Remarks  
 This is the value specified by the user in the Print dialog box, and it is stored in the `CPrintDialog` object referenced by the `m_pPD` member. If the user has not specified a value, the default is the first page of the document.  
  
## Requirements  
 **Header:** afxext.h  
  
## See Also  
 [CPrintInfo Structure](../vs140/CPrintInfo-Structure.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CPrintInfo::m_nCurPage](../vs140/CPrintInfo--m_nCurPage.md)   
 [CPrintInfo::m_pPD](../vs140/CPrintInfo--m_pPD.md)   
 [CPrintInfo::GetToPage](../vs140/CPrintInfo--GetToPage.md)