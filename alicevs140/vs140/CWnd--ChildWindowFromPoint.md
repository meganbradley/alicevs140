---
title: "CWnd::ChildWindowFromPoint"
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
ms.assetid: 41cd55e0-ea57-4d0b-bbdd-e56f2dc9db40
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CWnd::ChildWindowFromPoint
Determines which, if any, of the child windows belonging to `CWnd` contains the specified point.  
  
## Syntax  
  
```  
  
      CWnd* ChildWindowFromPoint(  
   POINT point   
) const;  
CWnd* ChildWindowFromPoint(  
   POINT point,  
   UINT nFlags   
) const;  
```  
  
#### Parameters  
 `point`  
 Specifies the client coordinates of the point to be tested.  
  
 *nflags*  
 Specifies which child windows to skip. This parameter can be a combination of the following values:  
  
|Value|Meaning|  
|-----------|-------------|  
|**CWP_ALL**|Do not skip any child windows|  
|**CWP_SKIPINVISIBLE**|Skip invisible child windows|  
|**CWP_SKIPDISABLED**|Skip disabled child windows|  
|**CWP_SKIPTRANSPARENT**|Skip transparent child windows|  
  
## Return Value  
 Identifies the child window that contains the point. It is **NULL** if the given point lies outside of the client area. If the point is within the client area but is not contained within any child window, `CWnd` is returned.  
  
 This member function will return a hidden or disabled child window that contains the specified point.  
  
 More than one window may contain the given point. However, this function returns only the `CWnd`* of the first window encountered that contains the point.  
  
 The `CWnd`* that is returned may be temporary and should not be stored for later use.  
  
## Example  
 [!CODE [NVC_MFCWindowing#77](../CodeSnippet/VS_Snippets_Cpp/NVC_MFCWindowing#77)]  
  
## Requirements  
 **Header:** afxwin.h  
  
## See Also  
 [CWnd Class](../vs140/CWnd-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CWnd::WindowFromPoint](../vs140/CWnd--WindowFromPoint.md)   
 [ChildWindowFromPoint](http://msdn.microsoft.com/library/windows/desktop/ms632676)