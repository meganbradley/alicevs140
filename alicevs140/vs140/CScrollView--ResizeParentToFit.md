---
title: "CScrollView::ResizeParentToFit"
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
ms.assetid: 17382950-a2bf-4710-870c-73b384b28f5e
caps.latest.revision: 14
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CScrollView::ResizeParentToFit
Call `ResizeParentToFit` to let the size of your view dictate the size of its frame window.  
  
## Syntax  
  
```  
  
      void ResizeParentToFit(   
   BOOL bShrinkOnly = TRUE    
);  
```  
  
#### Parameters  
 *bShrinkOnly*  
 The kind of resizing to perform. The default value, **TRUE**, shrinks the frame window if appropriate. Scroll bars will still appear for large views or small frame windows. A value of **FALSE** causes the view always to resize the frame window exactly. This can be somewhat dangerous since the frame window could get too big to fit inside the multiple document interface (MDI) frame window or the screen.  
  
## Remarks  
 This is recommended only for views in MDI child frame windows. Use `ResizeParentToFit` in the `OnInitialUpdate` handler function of your derived `CScrollView` class. For an example of this member function, see [CScrollView::SetScrollSizes](../vs140/CScrollView--SetScrollSizes.md).  
  
 `ResizeParentToFit` assumes that the size of the view window has been set. If the view window size has not been set when `ResizeParentToFit` is called, you will get an assertion. To ensure that this does not happen, make the following call before calling `ResizeParentToFit`:  
  
 [!CODE [NVC_MFCDocView#165](../CodeSnippet/VS_Snippets_Cpp/NVC_MFCDocView#165)]  
  
## Requirements  
 **Header:** afxwin.h  
  
## See Also  
 [CScrollView Class](../vs140/CScrollView-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CView::OnInitialUpdate](../vs140/CView--OnInitialUpdate.md)   
 [CScrollView::SetScrollSizes](../vs140/CScrollView--SetScrollSizes.md)