---
title: "CMFCVisualManagerOffice2003::OnDrawPaneCaption"
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
ms.assetid: 1289d1f9-ed82-49d7-bfc7-0de5e2ee25ad
caps.latest.revision: 11
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMFCVisualManagerOffice2003::OnDrawPaneCaption
The framework calls this method when it draws a caption for a [CDockablePane](../vs140/CDockablePane-Class.md) object.  
  
## Syntax  
  
```  
virtual COLORREF OnDrawPaneCaption(  
   CDC* pDC,  
   CDockablePane* pBar,  
   BOOL bActive,  
   CRect rectCaption,  
   CRect rectButtons  
);  
```  
  
#### Parameters  
 [in] `pDC`  
 A pointer to a device context.  
  
 [in] `pBar`  
 A pointer to a [CDockablePane](../vs140/CDockablePane-Class.md) object. The framework draws the caption for this pane.  
  
 [in] `bActive`  
 A Boolean parameter that indicates whether the control bar is active.  
  
 [in] `rectCaption`  
 A rectangle that specifies the boundaries of the caption.  
  
 [in] `rectButtons`  
 A rectangle that specifies the boundaries of the caption buttons.  
  
## Return Value  
 A [COLORREF](http://msdn.microsoft.com/library/windows/desktop/dd183449) parameter that indicates the text color of the caption.  
  
## Remarks  
  
## Requirements  
 **Header:** afxvisualmanageroffice2003.h  
  
## See Also  
 [CMFCVisualManagerOffice2003 Class](../vs140/CMFCVisualManagerOffice2003-Class.md)   
 [Hierarchy Chart (MFC Feature Pack)](../vs140/Hierarchy-Chart.md)