---
title: "COleControl::ClientToParent"
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
ms.assetid: 2c7c891b-0dd7-4526-a4ef-60a0ff1813f7
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# COleControl::ClientToParent
Translates the coordinates of `pPoint` into parent coordinates.  
  
## Syntax  
  
```  
  
      virtual void ClientToParent(  
   LPCRECT lprcBounds,  
   LPPOINT pPoint   
) const;  
```  
  
#### Parameters  
 `lprcBounds`  
 Pointer to the bounds of the OLE control within the container. Not the client area but the area of the entire control including borders and scroll bars.  
  
 `pPoint`  
 Pointer to the OLE client area point to be translated into the coordinates of the parent (container).  
  
## Remarks  
 On input `pPoint` is relative to the origin of the client area of the OLE control (upper left corner of the client area of the control). On output `pPoint` is relative to the origin of the parent (upper left corner of the container).  
  
## Requirements  
 **Header:** afxctl.h  
  
## See Also  
 [COleControl Class](../vs140/COleControl-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [COleControl::ParentToClient](../vs140/COleControl--ParentToClient.md)   
 [COleControl::GetClientOffset](../vs140/COleControl--GetClientOffset.md)