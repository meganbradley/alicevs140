---
title: "CMFCAcceleratorKey::CMFCAcceleratorKey"
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
ms.assetid: 3dd387c8-a753-40db-b587-5692ddddb198
caps.latest.revision: 11
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMFCAcceleratorKey::CMFCAcceleratorKey
Constructs a [CMFCAcceleratorKey](../vs140/CMFCAcceleratorKey-Class.md) object.  
  
## Syntax  
  
```  
CMFCAcceleratorKey();  
  
CMFCAcceleratorKey(  
   LPACCEL lpAccel   
);  
```  
  
#### Parameters  
 [in] `lpAccel`  
 A pointer to a shortcut key.  
  
## Remarks  
 If you do not provide a shortcut key when you create a `CMFCAccleratorKey`, use the [CMFCAcceleratorKey::SetAccelerator](../vs140/CMFCAcceleratorKey--SetAccelerator.md) method to associate a shortcut key with your `CMFCAcceleratorKey` object.  
  
## Requirements  
 **Header:** afxacceleratorkey.h  
  
## See Also  
 [CMFCAcceleratorKey Class](../vs140/CMFCAcceleratorKey-Class.md)   
 [Hierarchy Chart (MFC Feature Pack)](../vs140/Hierarchy-Chart.md)