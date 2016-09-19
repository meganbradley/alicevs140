---
title: "CSnapInItemImpl::AddMenuItems"
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
ms.assetid: 1623f900-15e9-4c8f-a2e1-77208e48bcbb
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CSnapInItemImpl::AddMenuItems
This method implements the Win32 function [IExtendContextMenu::AddMenuItems](http://msdn.microsoft.com/library/aa814841).  
  
## Syntax  
  
```  
  
      AddMenuItems(  
   LPCONTEXTMENUCALLBACK piCallback,  
   long *pInsertionAllowed,  
   DATA_OBJECT_TYPES type   
);  
```  
  
#### Parameters  
 *piCallback*  
 [in] Pointer to the **IContextMenuCallback** that can add items to the context menu.  
  
 `pInsertionAllowed`  
 [in, out] Identifies Microsoft Management Console (MMC)-defined, menu-item insertion points that can be used. This can be a combination of the following flags:  
  
-   **CCM_INSERTIONALLOWED_TOP** Items can be inserted at the top of a context menu.  
  
-   **CCM_INSERTIONALLOWED_NEW** Items can be inserted in the Create New submenu.  
  
-   **CCM_INSERTIONALLOWED_TASK** Items can be inserted in the Task submenu.  
  
-   **CCM_INSERTIONALLOWED_VIEW** Items can be inserted in the toolbar view menu or in the View submenu of the result pane context menu.  
  
 `type`  
 [in] Specifies the type of object. It can have one of the following values:  
  
-   **CCT_SCOPE** Data object for scope pane context.  
  
-   **CCT_RESULT** Data object for result pane context.  
  
-   **CCT_SNAPIN_MANAGER** Data object for snap-in manager context.  
  
-   **CCT_UNINITIALIZED** Data object has an invalid type.  
  
## Requirements  
 **Header:** atlsnap.h  
  
## See Also  
 [CSnapInItemImpl Class](../Topic/CSnapInItemImpl%20Class.md)