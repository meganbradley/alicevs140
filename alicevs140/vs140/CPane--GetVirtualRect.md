---
title: "CPane::GetVirtualRect"
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
ms.assetid: f1483f11-cc52-44bf-ae2b-57d013b6e093
caps.latest.revision: 18
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CPane::GetVirtualRect
Retrieves the *virtual rectangle* of the pane.  
  
## Syntax  
  
```  
void GetVirtualRect(  
   CRect& rectVirtual  
) const;  
```  
  
#### Parameters  
 [out] `rectVirtual`  
 A `CRect` object that is filled with the virtual rectangle.  
  
## Remarks  
 When a pane is moved, the framework stores the original position of the pane in a virtual rectangle. The framework can use the virtual rectangle to restore the original position of the pane.  
  
 Do not call methods that are related to virtual rectangles unless you are moving panes programmatically.  
  
## Requirements  
 **Header:** afxpane.h  
  
## See Also  
 [CPane Class](../vs140/CPane-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CPane::SetVirtualRect](../vs140/CPane--SetVirtualRect.md)