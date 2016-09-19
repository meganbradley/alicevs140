---
title: "COleClientItem::Deactivate"
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
ms.assetid: 114e621c-91b4-48fe-a96b-05f9f5a54024
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# COleClientItem::Deactivate
Call this function to deactivate the OLE item and free any associated resources.  
  
## Syntax  
  
```  
  
void Deactivate( );  
```  
  
## Remarks  
 You typically deactivate an in-place active OLE item when the user clicks the mouse on the client area outside the bounds of the item. Note that deactivating the OLE item will discard its undo state, making it impossible to call the [ReactivateAndUndo](../vs140/COleClientItem--ReactivateAndUndo.md) member function.  
  
 If your application supports undo, do not call `Deactivate`; instead, call [DeactivateUI](../vs140/COleClientItem--DeactivateUI.md).  
  
 For more information, see [IOleInPlaceObject::InPlaceDeactivate](http://msdn.microsoft.com/library/windows/desktop/ms679700) in the [!INCLUDE[winSDK](../vs140/includes/winSDK_md.md)].  
  
## Requirements  
 **Header:** afxole.h  
  
## See Also  
 [COleClientItem Class](../vs140/COleClientItem-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [COleClientItem::ReactivateAndUndo](../vs140/COleClientItem--ReactivateAndUndo.md)   
 [COleClientItem::DeactivateUI](../vs140/COleClientItem--DeactivateUI.md)