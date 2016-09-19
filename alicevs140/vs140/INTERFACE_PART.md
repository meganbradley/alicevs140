---
title: "INTERFACE_PART"
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
ms.topic: article
ms.assetid: 3a213520-e82c-45a2-96e2-3894ac8defeb
caps.latest.revision: 10
translation.priority.ht: 
  - de-de
  - ja-jp
---
# INTERFACE_PART
Used between the `BEGIN_INTERFACE_MAP` macro and the `END_INTERFACE_MAP` macro for each interface your object will support.  
  
## Syntax  
  
```  
  
INTERFACE_PART(  
theClass, iid, localClass)  
```  
  
#### Parameters  
 `theClass`  
 The name of the class that contains the interface map.  
  
 `iid`  
 The IID that is to be mapped to the embedded class.  
  
 *localClass*  
 The name of the local class.  
  
## Remarks  
 It allows you to map an IID to a member of the class indicated by `theClass` and *localClass*.  
  
 For more information on interface maps, see [Technical Note 38](../vs140/TN038--MFC-OLE-IUnknown-Implementation.md).  
  
## Requirements  
 **Header:** afxwin.h  
  
## See Also  
 [Macros and Globals](../vs140/MFC-Macros-and-Globals.md)   
 [BEGIN_INTERFACE_MAP](../vs140/BEGIN_INTERFACE_MAP.md)   
 [END_MESSAGE_MAP](../vs140/END_MESSAGE_MAP.md)