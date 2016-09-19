---
title: "CPrintInfo::m_nCurPage"
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
ms.assetid: 34ec516a-f7bb-4210-aa57-81991ad117cc
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CPrintInfo::m_nCurPage
Contains the number of the current page.  
  
## Remarks  
 The framework calls `CView::OnPrepareDC` and `CView::OnPrint` once for each page of the document, specifying a different value for this member each time; its values range from the value returned by `GetFromPage` to that returned by `GetToPage`. Use this member in your overrides of `CView::OnPrepareDC` and `CView::OnPrint` to print the specified page of the document.  
  
 When preview mode is first invoked, the framework reads the value of this member to determine which page of the document should be previewed initially. You can set the value of this member in your override of `CView::OnPreparePrinting` to maintain the user's current position in the document when entering preview mode. The `m_nCurPage` member is a public variable of type **UINT**.  
  
## Requirements  
 **Header:** afxext.h  
  
## See Also  
 [CPrintInfo Structure](../vs140/CPrintInfo-Structure.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CPrintInfo::GetFromPage](../vs140/CPrintInfo--GetFromPage.md)   
 [CPrintInfo::GetToPage](../vs140/CPrintInfo--GetToPage.md)   
 [CView::OnPrepareDC](../vs140/CView--OnPrepareDC.md)   
 [CView::OnPreparePrinting](../vs140/CView--OnPreparePrinting.md)   
 [CView::OnPrint](../vs140/CView--OnPrint.md)