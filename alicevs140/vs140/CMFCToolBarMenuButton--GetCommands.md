---
title: "CMFCToolBarMenuButton::GetCommands"
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
ms.assetid: d3db98d0-bd69-47a9-b73a-e140d4a5b2eb
caps.latest.revision: 15
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMFCToolBarMenuButton::GetCommands
Gives read-only access to the list of commands in the toolbar menu.  
  
## Syntax  
  
```  
const CObList& GetCommands() const;  
```  
  
## Return Value  
 A const reference to a [CObList](../vs140/CObList-Class.md) object, which contains a collection of [CMFCToolBarButton Class](../vs140/CMFCToolBarButton-Class.md) objects.  
  
## Remarks  
 A toolbar menu button can display a submenu. You can provide the list of commands in the submenu in the constructor or in [CMFCToolBarMenuButton::CreateFromMenu](../vs140/CMFCToolBarMenuButton--CreateFromMenu.md) as a handle to a menu (`HMENU`). The menu is converted to a list of objects that are derived from [CMFCToolBarButton Class](../vs140/CMFCToolBarButton-Class.md) and stored in the internal `CObList` object. You can access this list by calling this method.  
  
## Requirements  
 **Header:** afxtoolbarmenubutton.h  
  
## See Also  
 [CMFCToolBarMenuButton Class](../vs140/CMFCToolBarMenuButton-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)