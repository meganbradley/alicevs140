---
title: "CMFCToolBar::CalcFixedLayout"
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
ms.assetid: 3734d495-c9ec-4e3f-ae03-c9a55650dda3
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMFCToolBar::CalcFixedLayout
Calculates the horizontal size of the toolbar.  
  
## Syntax  
  
```  
virtual CSize CalcFixedLayout(  
   BOOL bStretch,  
   BOOL bHorz  
);  
```  
  
#### Parameters  
 [in] `bStretch`  
 `TRUE` to stretch the toolbar to the size of the parent frame.  
  
 [in] `bHorz`  
 `TRUE` to orient the toolbar horizontally; `FALSE` to orient the toolbar vertically.  
  
## Return Value  
 A `CSize` object that specifies the size of the toolbar.  
  
## Remarks  
 This method calculates the size of the toolbar by using the `CMFCToolBar::CalcLayout` method. It passes the `LM_STRETCH` flag for the `dwMode` parameter if `bStretch` is `TRUE`. It passes the `LM_HORZ` flag if `bHorz` is `TRUE`.  
  
 See the VisualStudioDemo sample for an example that uses this method.  
  
## Requirements  
 **Header:** afxtoolbar.h  
  
## See Also  
 [CMFCToolBar Class](../Topic/CMFCToolBar%20Class.md)   
 [Hierarchy Chart (MFC Feature Pack)](../vs140/Hierarchy-Chart.md)