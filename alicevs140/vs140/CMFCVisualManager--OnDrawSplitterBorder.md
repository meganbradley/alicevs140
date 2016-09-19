---
title: "CMFCVisualManager::OnDrawSplitterBorder"
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
ms.assetid: b40b7a7d-3fda-49b6-8d76-7459a6c8b485
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMFCVisualManager::OnDrawSplitterBorder
The framework calls this method when it draws the border around an instance of the [CSplitterWndEx Class](../vs140/CSplitterWndEx-Class.md).  
  
## Syntax  
  
```  
virtual void OnDrawSplitterBorder(  
   CDC* pDC,  
   CSplitterWndEx* pSplitterWnd,  
   CRect rect  
);  
```  
  
#### Parameters  
 [in] `pDC`  
 A pointer to a device context.  
  
 [in] `pSplitterWnd`  
 A pointer to a splitter window. The framework draws the border for this window.  
  
 [in] `rect`  
 A rectangle that specifies the boundaries of the splitter window.  
  
## Remarks  
 Override this method in a derived visual manager to customize the appearance of the border for a splitter window.  
  
## Requirements  
 **Header:** afxvisualmanager.h  
  
## See Also  
 [CMFCVisualManager Class](../vs140/CMFCVisualManager-Class.md)   
 [MFC Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CSplitterWndEx Class](../vs140/CSplitterWndEx-Class.md)