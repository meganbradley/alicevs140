---
title: "CMFCAcceleratorKeyAssignCtrl::IsKeyDefined"
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
ms.assetid: 96d3d8e9-e0c3-40cb-b25c-ff98ea918be4
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMFCAcceleratorKeyAssignCtrl::IsKeyDefined
Determines whether a shortcut key has been defined in the [CMFCAcceleratorKeyAssignCtrl](../vs140/CMFCAcceleratorKeyAssignCtrl-Class.md) object.  
  
## Syntax  
  
```  
BOOL IsKeyDefined() const;  
```  
  
## Return Value  
 Nonzero if the user has already pressed a valid combination of keys that define a shortcut key; otherwise 0.  
  
## Remarks  
 Use this function to determine whether the user entered a valid shortcut key in your `CMFCAcceleratorKeyAssignCtrl` object. If a shortcut key exists, you can use [CMFCAcceleratorKeyAssignCtrl::GetAccel](../vs140/CMFCAcceleratorKeyAssignCtrl--GetAccel.md) method to obtain the `ACCEL` structure associated with this shortcut key.  
  
## Requirements  
 **Header:**afxacceleratorkeyassignctrl.h  
  
## See Also  
 [CMFCAcceleratorKeyAssignCtrl Class](../vs140/CMFCAcceleratorKeyAssignCtrl-Class.md)   
 [Hierarchy Chart (MFC Feature Pack)](../vs140/Hierarchy-Chart.md)