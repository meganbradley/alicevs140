---
title: "COleIPFrameWndEx::GetDefaultResId"
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
ms.assetid: 0da3fe71-a3bf-4c41-8fdd-0d0c1c0f5fad
caps.latest.revision: 11
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# COleIPFrameWndEx::GetDefaultResId
Returns the menu resource ID that was specified when the frame window loaded the menu.  
  
## Syntax  
  
```  
UINT GetDefaultResId() const;  
```  
  
## Return Value  
 Returns the resource ID of the menu, or 0 if the frame window has no menu bar.  
  
## Remarks  
 Call this function to retrieve the resource ID that was specified when the frame window loaded the menu resource by calling `COleIPFrameWndEx::LoadFrame`.  
  
## Requirements  
 **Header:** afxoleipframewndex.h  
  
## See Also  
 [COleIPFrameWndEx Class](../vs140/COleIPFrameWndEx-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)