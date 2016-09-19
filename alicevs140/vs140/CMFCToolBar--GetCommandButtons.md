---
title: "CMFCToolBar::GetCommandButtons"
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
ms.assetid: 0e5fd302-9008-4d8f-8680-f8c0cf9f6bef
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMFCToolBar::GetCommandButtons
Returns a list of buttons that have a specified command ID from all toolbars in the application.  
  
## Syntax  
  
```  
static int GetCommandButtons(  
   UINT uiCmd,  
   CObList& listButtons   
);  
```  
  
#### Parameters  
 [in] `uiCmd`  
 The command ID of the buttons.  
  
 [out] `listButtons`  
 A reference to a [CObList](../vs140/CObList-Class.md) object that receives the list of toolbar buttons.  
  
## Return Value  
 The number of buttons that have the specified command ID.  
  
## Requirements  
 **Header:** afxtoolbar.h  
  
## See Also  
 [CMFCToolBar Class](../Topic/CMFCToolBar%20Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)