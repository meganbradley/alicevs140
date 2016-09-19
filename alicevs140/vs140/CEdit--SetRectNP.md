---
title: "CEdit::SetRectNP"
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
ms.assetid: 680d9e4e-3d32-44b5-a862-313ac8f5565f
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CEdit::SetRectNP
Call this function to set the formatting rectangle of a multiple-line edit control.  
  
## Syntax  
  
```  
  
      void SetRectNP(  
   LPCRECT lpRect   
);  
```  
  
#### Parameters  
 `lpRect`  
 Points to a `RECT` structure or `CRect` object that specifies the new dimensions of the rectangle.  
  
## Remarks  
 The formatting rectangle is the limiting rectangle of the text, which is independent of the size of the edit-control window.  
  
 `SetRectNP` is identical to the `SetRect` member function except that the edit-control window is not redrawn.  
  
 When the edit control is first created, the formatting rectangle is the same as the client area of the edit-control window. By calling the `SetRectNP` member function, an application can make the formatting rectangle larger or smaller than the edit-control window.  
  
 If the edit control has no scroll bar, text will be clipped, not wrapped, if the formatting rectangle is made larger than the window.  
  
 This member is processed only by multiple-line edit controls.  
  
 For more information, see [EM_SETRECTNP](http://msdn.microsoft.com/library/windows/desktop/bb761659) in the [!INCLUDE[winSDK](../vs140/includes/winSDK_md.md)].  
  
## Example  
 See the example for [CEdit::SetRect](../vs140/CEdit--SetRect.md).  
  
## Requirements  
 **Header:** afxwin.h  
  
## See Also  
 [CEdit Class](../vs140/CEdit-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CRect::CRect](../vs140/CRect--CRect.md)   
 [CRect::CopyRect](../vs140/CRect--CopyRect.md)   
 [CRect::operator =](../vs140/CRect--operator-=.md)   
 [CRect::SetRectEmpty](../vs140/CRect--SetRectEmpty.md)   
 [CEdit::GetRect](../vs140/CEdit--GetRect.md)   
 [CEdit::SetRect](../vs140/CEdit--SetRect.md)