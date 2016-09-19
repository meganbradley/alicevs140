---
title: "CGdiObject::FromHandle"
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
ms.assetid: 983a787e-404c-4874-aace-c91523ae147d
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CGdiObject::FromHandle
Returns a pointer to a `CGdiObject` object given a handle to a Windows GDI object.  
  
## Syntax  
  
```  
  
      static CGdiObject* PASCAL FromHandle(  
   HGDIOBJ hObject   
);  
```  
  
#### Parameters  
 `hObject`  
 A `HANDLE` to a Windows GDI object.  
  
## Return Value  
 A pointer to a `CGdiObject` that may be temporary or permanent.  
  
## Remarks  
 If a `CGdiObject` object is not already attached to the Windows GDI object, a temporary `CGdiObject` object is created and attached.  
  
 This temporary `CGdiObject` object is only valid until the next time the application has idle time in its event loop, at which time all temporary graphic objects are deleted. Another way of saying this is that the temporary object is only valid during the processing of one window message.  
  
## Requirements  
 **Header:** afxwin.h  
  
## See Also  
 [CGdiObject Class](../vs140/CGdiObject-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CGdiObject::DeleteTempMap](../vs140/CGdiObject--DeleteTempMap.md)