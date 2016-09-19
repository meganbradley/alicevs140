---
title: "COleClientItem::OnGetClipRect"
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
ms.assetid: 7efc44c9-3d70-49b0-aced-679d2730f414
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# COleClientItem::OnGetClipRect
The framework calls the `OnGetClipRect` member function to get the clipping-rectangle coordinates of the item that is being edited in place.  
  
## Syntax  
  
```  
  
      virtual void OnGetClipRect(  
   CRect& rClipRect   
);  
```  
  
#### Parameters  
 *rClipRect*  
 Pointer to an object of class [CRect](../vs140/CRect-Class.md) that will hold the clipping-rectangle coordinates of the item.  
  
## Remarks  
 Coordinates are in pixels relative to the container application window's client area.  
  
 The default implementation simply returns the client rectangle of the view on which the item is in-place active.  
  
## Requirements  
 **Header:** afxole.h  
  
## See Also  
 [COleClientItem Class](../vs140/COleClientItem-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [COleClientItem::OnActivate](../vs140/COleClientItem--OnActivate.md)