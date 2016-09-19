---
title: "CMFCAutoHideButton::Create"
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
ms.assetid: bde758f0-a846-4858-8c7e-7ea79c68dc03
caps.latest.revision: 16
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMFCAutoHideButton::Create
Creates and initializes an auto-hide button.  
  
## Syntax  
  
```  
virtual BOOL Create(  
   CMFCAutoHideBar* pParentBar,  
   CDockablePane* pAutoHideWnd,  
   DWORD dwAlignment   
);  
```  
  
#### Parameters  
 [in] `pParentBar`  
 A pointer to the parent toolbar.  
  
 [in] `pAutoHideWnd`  
 A pointer to a [CDockablePane](../vs140/CDockablePane-Class.md) object. This auto-hide button hides and shows that `CDockablePane`.  
  
 [in] `dwAlignment`  
 A value that specifies the alignment of the button with the main frame window.  
  
## Return Value  
 Nonzero if successful; otherwise 0.  
  
## Remarks  
 When you create a [CMFCAutoHideButton](../vs140/CMFCAutoHideButton-Class.md) object, you must associate the auto-hide button with a specific `CDockablePane`. The user can use the auto-hide button to hide and show the associated `CDockablePane`.  
  
 The `dwAlignment` parameter indicates where the auto-hide button resides in the application. The parameter can be any one of the following values:  
  
-   `CBRS_ALIGN_LEFT`  
  
-   `CBRS_ALIGN_RIGHT`  
  
-   `CBRS_ALIGN_TOP`  
  
-   `CBRS_ALIGN_BOTTOM`  
  
## Requirements  
 **Header:** afxautohidebutton.h  
  
## See Also  
 [CMFCAutoHideButton Class](../vs140/CMFCAutoHideButton-Class.md)   
 [Hierarchy Chart (MFC Feature Pack)](../vs140/Hierarchy-Chart.md)