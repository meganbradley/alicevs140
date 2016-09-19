---
title: "CMFCAcceleratorKeyAssignCtrl::GetAccel"
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
ms.assetid: c784cf3f-9afc-4aab-b3fe-f2903ae0ce57
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMFCAcceleratorKeyAssignCtrl::GetAccel
Retrieves the `ACCEL` structure for a shortcut key pressed in the [CMFCAcceleratorKeyAssignCtrl](../vs140/CMFCAcceleratorKeyAssignCtrl-Class.md) object.  
  
## Syntax  
  
```  
ACCEL const* GetAccel() const;  
```  
  
## Return Value  
 An `ACCEL` structure that describes the shortcut key.  
  
## Remarks  
 Use this function to retrieve the `ACCEL` structure for a shortcut key that the user entered into your `CMFCAcceleratorKeyAssignCtrl` object.  
  
## Requirements  
 **Header:**afxacceleratorkeyassignctrl.h  
  
## See Also  
 [CMFCAcceleratorKeyAssignCtrl Class](../vs140/CMFCAcceleratorKeyAssignCtrl-Class.md)   
 [Hierarchy Chart (MFC Feature Pack)](../vs140/Hierarchy-Chart.md)