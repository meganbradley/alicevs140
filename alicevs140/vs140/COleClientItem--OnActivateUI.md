---
title: "COleClientItem::OnActivateUI"
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
ms.assetid: 9c5554d2-e7bd-4ccc-b772-22d5c16f99bc
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# COleClientItem::OnActivateUI
The framework calls `OnActivateUI` when the object has entered the active UI state.  
  
## Syntax  
  
```  
  
virtual void OnActivateUI( );  
```  
  
## Remarks  
 The object has now installed its tool bar and menus.  
  
 The default implementation remembers the server's `HWND` for later **GetServerWindow** calls.  
  
## Requirements  
 **Header:** afxole.h  
  
## See Also  
 [COleClientItem Class](../vs140/COleClientItem-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [COleClientItem::OnDeactivate](../vs140/COleClientItem--OnDeactivate.md)   
 [COleClientItem::OnDeactivateUI](../vs140/COleClientItem--OnDeactivateUI.md)   
 [COleClientItem::OnActivate](../vs140/COleClientItem--OnActivate.md)   
 [COleClientItem::CanActivate](../vs140/COleClientItem--CanActivate.md)