---
title: "CPrintInfo::GetMaxPage"
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
ms.assetid: 52a460ac-6bf7-46ba-9b15-9c0b8740fdee
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CPrintInfo::GetMaxPage
Call this function to retrieve the number of the last page of the document.  
  
## Syntax  
  
```  
  
UINT GetMaxPage( ) const;  
```  
  
## Return Value  
 The number of the last page of the document.  
  
## Remarks  
 This value is stored in the `CPrintDialog` object referenced by the `m_pPD` member.  
  
## Requirements  
 **Header:** afxext.h  
  
## See Also  
 [CPrintInfo Structure](../vs140/CPrintInfo-Structure.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CPrintInfo::m_nCurPage](../vs140/CPrintInfo--m_nCurPage.md)   
 [CPrintInfo::m_pPD](../vs140/CPrintInfo--m_pPD.md)   
 [CPrintInfo::GetMinPage](../vs140/CPrintInfo--GetMinPage.md)   
 [CPrintInfo::SetMaxPage](../vs140/CPrintInfo--SetMaxPage.md)   
 [CPrintInfo::SetMinPage](../vs140/CPrintInfo--SetMinPage.md)