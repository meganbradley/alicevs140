---
title: "CMFCDynamicLayout::GetWindowRect"
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
ms.assetid: 8f8c7c60-afc3-4daa-afe7-7fc343228ed3
caps.latest.revision: 6
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMFCDynamicLayout::GetWindowRect
Retrieves the rectangle for the window's current client area.  
  
## Syntax  
  
```  
  
      void GetHostWndRect(  
    CRect& rect,  
);  
```  
  
#### Parameters  
 `rect`  
 After the function returns, this parameter contains the bounding rectangle of the layout area. This is an out parameter; the input value is overwritten.  
  
## Remarks  
  
## Requirements  
 **Header:** afxlayout.h  
  
## See Also  
 [CMFCDynamicLayout Class](../vs140/CMFCDynamicLayout-Class.md)