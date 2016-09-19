---
title: "CBasePane::EnableGripper"
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
ms.assetid: b4627de9-87e7-44ab-9afb-bec67550cfa1
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CBasePane::EnableGripper
Enables or disables the gripper. If the gripper is enabled, the user can drag it to reposition the pane.  
  
## Syntax  
  
```  
virtual void EnableGripper(  
   BOOL bEnable   
);  
```  
  
#### Parameters  
 [in] `bEnable`  
 `TRUE` to enable the gripper; `FALSE` to disable it.  
  
## Remarks  
 The framework uses this method to enable a gripper instead of using the `WS_CAPTION` style.  
  
## Requirements  
 **Header:** afxbasepane.h  
  
## See Also  
 [CBasePane Class](../vs140/CBasePane-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)