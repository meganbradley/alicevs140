---
title: "CPrintInfo::SetMaxPage"
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
ms.assetid: 5d230ef9-7806-436c-84ec-f0c45a0c1725
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CPrintInfo::SetMaxPage
Call this function to specify the number of the last page of the document.  
  
## Syntax  
  
```  
  
      void SetMaxPage(  
   UINT nMaxPage   
);  
```  
  
#### Parameters  
 *nMaxPage*  
 Number of the last page of the document.  
  
## Remarks  
 This value is stored in the `CPrintDialog` object referenced by the `m_pPD` member. If the length of the document is known before it is printed, call this function from your override of `CView::OnPreparePrinting`. If the length of the document depends on a setting specified by the user in the Print dialog box, call this function from your override of `CView::OnBeginPrinting`. If the length of the document is not known until it is printed, use the `m_bContinuePrinting` member to control the print loop.  
  
## Example  
 See the example for [CView::OnPreparePrinting](../vs140/CView--OnPreparePrinting.md).  
  
## Requirements  
 **Header:** afxext.h  
  
## See Also  
 [CPrintInfo Structure](../vs140/CPrintInfo-Structure.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CPrintInfo::m_bContinuePrinting](../vs140/CPrintInfo--m_bContinuePrinting.md)   
 [CPrintInfo::m_nCurPage](../vs140/CPrintInfo--m_nCurPage.md)   
 [CPrintInfo::m_pPD](../vs140/CPrintInfo--m_pPD.md)   
 [CPrintInfo::GetMinPage](../vs140/CPrintInfo--GetMinPage.md)   
 [CPrintInfo::GetToPage](../vs140/CPrintInfo--GetToPage.md)   
 [CPrintInfo::SetMinPage](../vs140/CPrintInfo--SetMinPage.md)   
 [CView::OnBeginPrinting](../vs140/CView--OnBeginPrinting.md)   
 [CView::OnPreparePrinting](../vs140/CView--OnPreparePrinting.md)