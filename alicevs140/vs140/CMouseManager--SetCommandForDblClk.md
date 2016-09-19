---
title: "CMouseManager::SetCommandForDblClk"
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
ms.assetid: 982bf0fa-198a-4dc8-b964-dba66f60da96
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMouseManager::SetCommandForDblClk
Associates a custom command with a view that is first registered with the mouse manager.  
  
## Syntax  
  
```  
void SetCommandForDblClk(  
   int iViewId,  
   UINT uiCmd   
);  
```  
  
#### Parameters  
 [in] `iViewId`  
 The view identifier.  
  
 [in] `uiCmd`  
 The command identifier.  
  
## Remarks  
 In order to associate a custom command with a view, you must first register the view by using [CMouseManager::AddView](../vs140/CMouseManager--AddView.md). The `AddView` method requires a view identifier as an input parameter. Once you register a view, you can call `CMouseManager::SetCommandForDblClk` with the same view identifier input parameter that you supplied to `AddView`. Thereafter, when the user double-clicks the mouse in the registered view, the application will execute the command indicated by `uiCmd.` To support the custom mouse behavior, you will also need to customize the view registered with the mouse manager. For more information about custom mouse behavior, see [Keyboard and Mouse Customization](../vs140/Keyboard-and-Mouse-Customization.md).  
  
 If `uiCmd` is set to 0, the specified view is no longer associated with a command.  
  
## Requirements  
 **Header:** afxmousemanager.h  
  
## See Also  
 [CMouseManager Class](../vs140/CMouseManager-Class.md)   
 [Hierarchy Chart (MFC Feature Pack)](../vs140/Hierarchy-Chart.md)   
 [Keyboard and Mouse Customization](../vs140/Keyboard-and-Mouse-Customization.md)