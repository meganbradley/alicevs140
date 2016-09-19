---
title: "CPaneFrameWnd::CalcBorderSize"
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
ms.assetid: b1e09869-ac7a-4e9b-a097-ebb7d3bc7c9c
caps.latest.revision: 9
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CPaneFrameWnd::CalcBorderSize
Calculates the size of the borders for a miniframe window.  
  
## Syntax  
  
```  
virtual void CalcBorderSize(  
    CRect& rectBorderSize   
) const;  
```  
  
#### Parameters  
 [out] `rectBorderSize`  
 Contains the size, in pixels, of the border of the miniframe window.  
  
## Remarks  
 This method is called by the framework to calculate the size of the border of a miniframe window. The returned size depends on whether a miniframe window contains a toolbar or a [CDockablePane](../vs140/CDockablePane-Class.md).  
  
## Requirements  
 **Header:** afxPaneFrameWnd.h  
  
## See Also  
 [CPaneFrameWnd Class](../vs140/CPaneFrameWnd-Class.md)   
 [MFC Hierarchy Chart](../vs140/Hierarchy-Chart.md)