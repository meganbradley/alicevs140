---
title: "CMFCVisualManager::OnDrawOutlookBarSplitter"
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
ms.assetid: c9016780-6c59-4a17-929b-24cc0aa3d697
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMFCVisualManager::OnDrawOutlookBarSplitter
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
 **Header:** afxvisualmanager.h  
  
## See Also  
 [CMFCVisualManager Class](../vs140/CMFCVisualManager-Class.md)   
 [MFC Hierarchy Chart](../vs140/Hierarchy-Chart.md)