---
title: "CWnd::BeginPaint"
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
ms.assetid: c61f03d7-7d43-4da5-8149-7c415e0df109
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CWnd::BeginPaint
Prepares `CWnd` for painting and fills a `PAINTSTRUCT` data structure with information about the painting.  
  
## Syntax  
  
```  
  
      CDC* BeginPaint(  
   LPPAINTSTRUCT lpPaint   
);  
```  
  
#### Parameters  
 `lpPaint`  
 Points to the [PAINTSTRUCT](../vs140/PAINTSTRUCT-Structure.md) structure that is to receive painting information.  
  
## Return Value  
 Identifies the device context for `CWnd`. The pointer may be temporary and should not be stored beyond the scope of [EndPaint](../vs140/CWnd--EndPaint.md).  
  
## Remarks  
 The paint structure contains a [RECT](../vs140/RECT-Structure.md) data structure that has the smallest rectangle that completely encloses the update region and a flag that specifies whether the background has been erased.  
  
 The update region is set by the [Invalidate](../vs140/CWnd--Invalidate.md), [InvalidateRect](../vs140/CWnd--InvalidateRect.md), or [InvalidateRgn](../vs140/CWnd--InvalidateRgn.md) member functions and by the system after it sizes, moves, creates, scrolls, or performs any other operation that affects the client area. If the update region is marked for erasing, `BeginPaint` sends an [WM_ONERASEBKGND](../vs140/CWnd--OnEraseBkgnd.md) message.  
  
 Do not call the `BeginPaint` member function except in response to a [WM_PAINT](../vs140/CWnd--OnPaint.md) message. Each call to the `BeginPaint` member function must have a matching call to the [EndPaint](../vs140/CWnd--EndPaint.md) member function. If the caret is in the area to be painted, the `BeginPaint` member function automatically hides the caret to prevent it from being erased.  
  
## Example  
 [!CODE [NVC_MFCWindowing#70](../CodeSnippet/VS_Snippets_Cpp/NVC_MFCWindowing#70)]  
  
## Requirements  
 **Header:** afxwin.h  
  
## See Also  
 [CWnd Class](../vs140/CWnd-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CWnd::EndPaint](../vs140/CWnd--EndPaint.md)   
 [CWnd::Invalidate](../vs140/CWnd--Invalidate.md)   
 [CWnd::InvalidateRgn](../vs140/CWnd--InvalidateRgn.md)   
 [BeginPaint](http://msdn.microsoft.com/library/windows/desktop/dd183362)   
 [CPaintDC Class](../vs140/CPaintDC-Class.md)