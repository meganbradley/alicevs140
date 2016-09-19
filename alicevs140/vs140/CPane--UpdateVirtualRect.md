---
title: "CPane::UpdateVirtualRect"
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
ms.assetid: b7a2ea8b-831f-42cc-b892-2c5cbcce2f3e
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CPane::UpdateVirtualRect
Updates the virtual rectangle.  
  
## Syntax  
  
```  
void UpdateVirtualRect();  
void UpdateVirtualRect(  
   CPoint ptOffset  
);  
void UpdateVirtualRect(  
   CSize sizeNew  
);  
```  
  
#### Parameters  
 [in] `ptOffset`  
 A `CPoint` object that specifies an offset by which to shift the pane.  
  
 [in] `sizeNew`  
 A `CSize` object that specifies a new size for the  pane.  
  
## Remarks  
 The first overload sets the virtual rectangle by using the current position and size of the pane.  
  
 The second overload shifts the virtual rectangle by the amount that is specified by `ptOffset`.  
  
 The third overload sets the virtual rectangle by using the current position of the pane and the size that is specified by `sizeNew`.  
  
## Requirements  
 **Header:** afxpane.h  
  
## See Also  
 [CPane Class](../vs140/CPane-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)