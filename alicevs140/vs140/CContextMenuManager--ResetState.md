---
title: "CContextMenuManager::ResetState"
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
ms.assetid: ae5c197b-6c89-4a0e-9f23-4ee3654ae9a8
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CContextMenuManager::ResetState
Clears all items from the shortcut menus associated with the [CContextMenuManager Class](../vs140/CContextMenuManager-Class.md).  
  
## Syntax  
  
```  
virtual BOOL ResetState();  
```  
  
## Return Value  
 `TRUE` if the method is successful; `FALSE` if a failure occurs.  
  
## Remarks  
 This method clears the pop-up menus and removes them from the `CContextMenuManager`.  
  
## Requirements  
 **Header:** afxcontextmenumanager.h  
  
## See Also  
 [CContextMenuManager Class](../vs140/CContextMenuManager-Class.md)   
 [Hierarchy Chart (MFC Feature Pack)](../vs140/Hierarchy-Chart.md)