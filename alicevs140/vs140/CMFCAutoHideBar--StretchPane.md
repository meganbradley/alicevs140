---
title: "CMFCAutoHideBar::StretchPane"
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
ms.assetid: b1c00693-d67b-4594-be40-83d7379d2b4d
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMFCAutoHideBar::StretchPane
Resizes the auto-hide bar in its collapsed state to fit the `CMFCAutoHideButton` object.  
  
## Syntax  
  
```  
 virtual CSize StretchPane(  
    int nLength,   
    BOOL bVert  
);  
```  
  
#### Parameters  
 [in] `nLength`  
 The value is unused in the base implementation. In derived implementations, use this value to indicate the length of the resized pane.  
  
 [in] `bVert`  
 The value is unused in the base implementation. In derived implementations, use  `TRUE` to handle the case where the auto-hide bar is collapsed vertically, and  `FALSE` for the case where the auto-hide bar is collapsed horizontally.  
  
## Return Value  
 The resulting size of the resized pane.  
  
## Remarks  
 Derived classes can override this method to customize the behavior.  
  
## Requirements  
 **Header:** afxautohidebar.h  
  
## See Also  
 [CMFCAutoHideBar Class](../vs140/CMFCAutoHideBar-Class.md)   
 [Hierarchy Chart (MFC Feature Pack)](../vs140/Hierarchy-Chart.md)