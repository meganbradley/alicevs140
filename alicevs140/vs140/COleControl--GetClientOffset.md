---
title: "COleControl::GetClientOffset"
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
ms.assetid: 4b52e200-7d08-49c7-8bae-b3f5db9c87cb
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# COleControl::GetClientOffset
Retrieves the difference between the upper left corner of the control's rectangular area and the upper left corner of its client area.  
  
## Syntax  
  
```  
  
      virtual void GetClientOffset(  
   long* pdxOffset,  
   long* pdyOffset   
) const;  
```  
  
#### Parameters  
 *pdxOffset*  
 Pointer to the horizontal offset of the OLE control's client area.  
  
 *pdyOffset*  
 Pointer to the vertical offset of the OLE control's client area.  
  
## Remarks  
 The OLE control has a rectangular area within its container. The client area of the control is the control area excluding borders and scroll bars. The offset retrieved by `GetClientOffset` is the difference between the upper left corner of the control's rectangular area and the upper left corner of its client area. If your control has non-client elements other than the standard borders and scrollbars, override this member function to specify the offset.  
  
## Requirements  
 **Header:** afxctl.h  
  
## See Also  
 [COleControl Class](../vs140/COleControl-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [COleControl::ParentToClient](../vs140/COleControl--ParentToClient.md)   
 [COleControl::ClientToParent](../vs140/COleControl--ClientToParent.md)