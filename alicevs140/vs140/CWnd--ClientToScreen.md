---
title: "CWnd::ClientToScreen"
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
ms.assetid: 0c4a4b3b-48f2-4792-b94a-f34c6f45aee6
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CWnd::ClientToScreen
Converts the client coordinates of a given point or rectangle on the display to screen coordinates.  
  
## Syntax  
  
```  
  
      void ClientToScreen(  
   LPPOINT lpPoint   
) const;  
void ClientToScreen(  
   LPRECT lpRect   
) const;  
```  
  
#### Parameters  
 `lpPoint`  
 Points to a [POINT](../vs140/POINT-Structure.md) structure or `CPoint` object that contains the client coordinates to be converted.  
  
 `lpRect`  
 Points to a [RECT](../vs140/RECT-Structure.md) structure or `CRect` object that contains the client coordinates to be converted.  
  
## Remarks  
 The `ClientToScreen` member function uses the client coordinates in the **POINT** or `RECT` structure or the `CPoint` or `CRect` object pointed to by `lpPoint` or `lpRect` to compute new screen coordinates; it then replaces the coordinates in the structure with the new coordinates. The new screen coordinates are relative to the upper-left corner of the system display.  
  
 The `ClientToScreen` member function assumes that the given point or rectangle is in client coordinates.  
  
## Example  
 [!CODE [NVC_MFCWindowing#78](../CodeSnippet/VS_Snippets_Cpp/NVC_MFCWindowing#78)]  
  
## Requirements  
 **Header:** afxwin.h  
  
## See Also  
 [CWnd Class](../vs140/CWnd-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CWnd::ScreenToClient](../vs140/CWnd--ScreenToClient.md)   
 [ClientToScreen](http://msdn.microsoft.com/library/windows/desktop/dd183434)