---
title: "CMFCVisualManagerOffice2003::OnDrawOutlookBarSplitter"
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
ms.assetid: 819dc7df-3a52-4791-bb86-10359f9b7534
caps.latest.revision: 11
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMFCVisualManagerOffice2003::OnDrawOutlookBarSplitter
The framework calls this method when it draws the splitter for an Outlook bar.  
  
## Syntax  
  
```  
virtual void OnDrawOutlookBarSplitter(  
   CDC* pDC,  
   CRect rectSplitter  
);  
```  
  
#### Parameters  
 [in] `pDC`  
 A pointer to a device context.  
  
 [in] `rectSplitter`  
 A rectangle that specifies the boundaries of the splitter.  
  
## Remarks  
 Override this method in a derived visual manager to customize the appearance of splitters on an Outlook bar.  
  
## Requirements  
 **Header:** afxvisualmanageroffice2003.h  
  
## See Also  
 [CMFCVisualManagerOffice2003 Class](../vs140/CMFCVisualManagerOffice2003-Class.md)   
 [Hierarchy Chart (MFC Feature Pack)](../vs140/Hierarchy-Chart.md)