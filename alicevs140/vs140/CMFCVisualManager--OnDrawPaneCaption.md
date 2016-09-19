---
title: "CMFCVisualManager::OnDrawPaneCaption"
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
ms.assetid: b692ee97-f5b5-43ed-bb40-ff2dd7484d75
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMFCVisualManager::OnDrawPaneCaption
The framework calls this method when it draws a caption for an instance of the [CDockablePane Class](../vs140/CDockablePane-Class.md).  
  
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
 A pointer to a `CDockablePane` object. The framework draws the caption for this pane.  
  
 [in] `bActive`  
 A Boolean parameter that indicates whether the control bar is active.  
  
 [in] `rectCaption`  
 A rectangle that specifies the boundaries of the caption.  
  
 [in] `rectButtons`  
 A rectangle that specifies the boundaries of the caption buttons.  
  
## Return Value  
 A [COLORREF](http://msdn.microsoft.com/library/windows/desktop/dd183449) parameter that indicates the text color of the caption.  
  
## Remarks  
 Override this method in a derived visual manager to customize the appearance of pane captions.  
  
## Requirements  
 **Header:** afxvisualmanager.h  
  
## See Also  
 [CMFCVisualManager Class](../vs140/CMFCVisualManager-Class.md)   
 [MFC Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CDockablePane Class](../vs140/CDockablePane-Class.md)