---
title: "COleClientItem::DeactivateUI"
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
ms.assetid: 54ba249b-66d9-4f40-a68e-f15c4e3e3ac6
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# COleClientItem::DeactivateUI
Call this function when the user deactivates an item that was activated in place.  
  
## Syntax  
  
```  
  
void DeactivateUI( );  
```  
  
## Remarks  
 This function restores the container application's user interface to its original state, hiding any menus and other controls that were created for in-place activation.  
  
 This function does not flush the undo state information for the item. That information is retained so that [ReactivateAndUndo](../vs140/COleClientItem--ReactivateAndUndo.md) can later be used to execute an undo command in the server application, in case the container's undo command is chosen immediately after deactivating the item.  
  
 For more information, see [IOleInPlaceObject::InPlaceDeactivate](http://msdn.microsoft.com/library/windows/desktop/ms679700) in the [!INCLUDE[winSDK](../vs140/includes/winSDK_md.md)].  
  
## Requirements  
 **Header:** afxole.h  
  
## See Also  
 [COleClientItem Class](../vs140/COleClientItem-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [COleClientItem::ReactivateAndUndo](../vs140/COleClientItem--ReactivateAndUndo.md)   
 [COleClientItem::Activate](../vs140/COleClientItem--Activate.md)