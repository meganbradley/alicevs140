---
title: "CPrintInfo::GetToPage"
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
ms.assetid: 17b1203a-e6e4-4431-9d24-a622e23405a3
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CPrintInfo::GetToPage
Call this function to retrieve the number of the last page to be printed.  
  
## Syntax  
  
```  
  
UINT GetToPage( ) const;  
```  
  
## Return Value  
 The number of the last page to be printed.  
  
## Remarks  
 This is the value specified by the user in the Print dialog box, and it is stored in the `CPrintDialog` object referenced by the `m_pPD` member. If the user has not specified a value, the default is the last page of the document.  
  
## Requirements  
 **Header:** afxext.h  
  
## See Also  
 [CPrintInfo Structure](../vs140/CPrintInfo-Structure.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CPrintInfo::m_nCurPage](../vs140/CPrintInfo--m_nCurPage.md)   
 [CPrintInfo::m_pPD](../vs140/CPrintInfo--m_pPD.md)   
 [CPrintInfo::GetFromPage](../vs140/CPrintInfo--GetFromPage.md)