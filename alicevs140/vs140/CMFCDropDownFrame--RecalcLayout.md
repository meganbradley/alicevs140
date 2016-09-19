---
title: "CMFCDropDownFrame::RecalcLayout"
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
ms.assetid: 47569ea3-8a26-43e6-b2e2-c4f2dffcb63e
caps.latest.revision: 11
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMFCDropDownFrame::RecalcLayout
Repositions the drop-down frame.  
  
## Syntax  
  
```  
virtual void RecalcLayout(  
   BOOL bNotify = TRUE  
);  
```  
  
#### Parameters  
  
|||  
|-|-|  
|Parameter|Description|  
|[in] `bNotify`|Unused.|  
  
## Remarks  
 The framework calls this method when the drop-down frame is created or the parent window is resized. This method calculates the position and size of the drop-down frame by using the position and size of the parent window.  
  
## Requirements  
 **Header:** afxdropdowntoolbar.h  
  
## See Also  
 [CMFCDropDownFrame Class](../vs140/CMFCDropDownFrame-Class.md)   
 [Hierarchy Chart (MFC Feature Pack)](../vs140/Hierarchy-Chart.md)