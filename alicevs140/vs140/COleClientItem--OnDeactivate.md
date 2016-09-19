---
title: "COleClientItem::OnDeactivate"
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
ms.assetid: 99ecb116-098c-43f4-a242-3372ebc141fa
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# COleClientItem::OnDeactivate
Called by the framework when the OLE item transitions from the in-place active state (`activeState`) to the loaded state, meaning that it is deactivated after an in-place activation.  
  
## Syntax  
  
```  
  
virtual void OnDeactivate( );  
```  
  
## Remarks  
 Note that this function is called to indicate that the OLE item is closed, not that its user interface has been removed from the container application. When that happens, the [OnDeactivateUI](../vs140/COleClientItem--OnDeactivateUI.md) member function is called.  
  
 The default implementation calls the [OnChange](../vs140/COleClientItem--OnChange.md) member function with **OLE_CHANGEDSTATE** as a parameter. Override this function to perform custom processing when an in-place active item is deactivated. For example, if you support the undo command in your container application, you can override this function to discard the undo state, indicating that the last operation performed on the OLE item cannot be undone once the item is deactivated.  
  
## Requirements  
 **Header:** afxole.h  
  
## See Also  
 [COleClientItem Class](../vs140/COleClientItem-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [COleClientItem::OnGetWindowContext](../vs140/COleClientItem--OnGetWindowContext.md)   
 [COleClientItem::OnDeactivateUI](../vs140/COleClientItem--OnDeactivateUI.md)   
 [COleClientItem::OnActivateUI](../vs140/COleClientItem--OnActivateUI.md)   
 [COleClientItem::OnActivate](../vs140/COleClientItem--OnActivate.md)   
 [COleClientItem::CanActivate](../vs140/COleClientItem--CanActivate.md)   
 [CDocTemplate::SetContainerInfo](../vs140/CDocTemplate--SetContainerInfo.md)