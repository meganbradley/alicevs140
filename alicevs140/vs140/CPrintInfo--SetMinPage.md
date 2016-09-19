---
title: "CPrintInfo::SetMinPage"
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
ms.assetid: 30a2f965-3ada-409d-98fd-a4dd392a65b7
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CPrintInfo::SetMinPage
Call this function to specify the number of the first page of the document.  
  
## Syntax  
  
```  
  
      void SetMinPage(  
   UINT nMinPage   
);  
```  
  
#### Parameters  
 *nMinPage*  
 Number of the first page of the document.  
  
## Remarks  
 Page numbers normally start at 1. This value is stored in the `CPrintDialog` object referenced by the `m_pPD` member.  
  
## Requirements  
 **Header:** afxext.h  
  
## See Also  
 [CPrintInfo Structure](../vs140/CPrintInfo-Structure.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CPrintInfo::m_nCurPage](../vs140/CPrintInfo--m_nCurPage.md)   
 [CPrintInfo::m_pPD](../vs140/CPrintInfo--m_pPD.md)   
 [CPrintInfo::GetMaxPage](../vs140/CPrintInfo--GetMaxPage.md)   
 [CPrintInfo::GetMinPage](../vs140/CPrintInfo--GetMinPage.md)   
 [CPrintInfo::SetMaxPage](../vs140/CPrintInfo--SetMaxPage.md)