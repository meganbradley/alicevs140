---
title: "COleClientItem::OnActivate"
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
ms.assetid: 10bfc777-597e-4345-a366-4df5ada12012
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# COleClientItem::OnActivate
Called by the framework to notify the item that it has just been activated in place.  
  
## Syntax  
  
```  
  
virtual void OnActivate( );  
```  
  
## Remarks  
 Note that this function is called to indicate that the server is running, not to indicate that its user interface has been installed in the container application. At this point, the object does not have an active user interface (is not `activeUIState`). It has not installed its menus or toolbar. The [OnActivateUI](../vs140/COleClientItem--OnActivateUI.md) member function is called when that happens.  
  
 The default implementation calls the [OnChange](../vs140/COleClientItem--OnChange.md) member function with **OLE_CHANGEDSTATE** as a parameter. Override this function to perform custom processing when an item becomes in-place active.  
  
## Requirements  
 **Header:** afxole.h  
  
## See Also  
 [COleClientItem Class](../vs140/COleClientItem-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [COleClientItem::OnDeactivate](../vs140/COleClientItem--OnDeactivate.md)   
 [COleClientItem::OnDeactivateUI](../vs140/COleClientItem--OnDeactivateUI.md)   
 [COleClientItem::OnActivateUI](../vs140/COleClientItem--OnActivateUI.md)   
 [COleClientItem::CanActivate](../vs140/COleClientItem--CanActivate.md)