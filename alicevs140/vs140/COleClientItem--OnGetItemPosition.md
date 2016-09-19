---
title: "COleClientItem::OnGetItemPosition"
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
ms.assetid: 484d6ec2-6050-4aac-8ccc-1a01d5909c4b
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# COleClientItem::OnGetItemPosition
The framework calls the `OnGetItemPosition` member function to get the coordinates of the item that is being edited in place.  
  
## Syntax  
  
```  
  
      virtual void OnGetItemPosition(  
   CRect& rPosition   
);  
```  
  
#### Parameters  
 `rPosition`  
 Reference to the [CRect](../vs140/CRect-Class.md) object that will contain the item's position coordinates.  
  
## Remarks  
 Coordinates are in pixels relative to the container application window's client area.  
  
 The default implementation of this function does nothing. Applications that support in-place editing require its implementation.  
  
## Requirements  
 **Header:** afxole.h  
  
## See Also  
 [COleClientItem Class](../vs140/COleClientItem-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [COleClientItem::OnActivate](../vs140/COleClientItem--OnActivate.md)   
 [COleClientItem::OnActivateUI](../vs140/COleClientItem--OnActivateUI.md)