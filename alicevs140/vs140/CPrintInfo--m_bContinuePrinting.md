---
title: "CPrintInfo::m_bContinuePrinting"
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
ms.assetid: 467c1abc-22f9-46d4-85ec-175f53728f5c
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CPrintInfo::m_bContinuePrinting
Contains a flag indicating whether the framework should continue the print loop.  
  
## Remarks  
 If you are doing print-time pagination, you can set this member to **FALSE** in your override of `CView::OnPrepareDC` once the end of the document has been reached. You do not have to modify this variable if you have specified the length of the document at the beginning of the print job using the `SetMaxPage` member function. The `m_bContinuePrinting` member is a public variable of type **BOOL**.  
  
## Requirements  
 **Header:** afxext.h  
  
## See Also  
 [CPrintInfo Structure](../vs140/CPrintInfo-Structure.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CPrintInfo::SetMaxPage](../vs140/CPrintInfo--SetMaxPage.md)   
 [CView::OnPrepareDC](../vs140/CView--OnPrepareDC.md)