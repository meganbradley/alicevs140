---
title: "CComPolyObject::CComPolyObject"
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
ms.assetid: f9241802-dbc8-42db-a1be-a357cd158481
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CComPolyObject::CComPolyObject
The constructor.  
  
## Syntax  
  
```  
  
      CComPolyObject(  
   void* pv   
);  
```  
  
#### Parameters  
 `pv`  
 [in] A pointer to the outer unknown if the object is to be aggregated, or **NULL** if the object if the object is not aggregated.  
  
## Remarks  
 Initializes the `CComContainedObject` data member, [m_contained](../vs140/CComPolyObject--m_contained.md), and increments the module lock count.  
  
 The destructor decrements the module lock count.  
  
## Requirements  
 **Header:** atlcom.h  
  
## See Also  
 [CComPolyObject Class](../vs140/CComPolyObject-Class.md)   
 [CComPolyObject::FinalConstruct](../vs140/CComPolyObject--FinalConstruct.md)   
 [CComPolyObject::FinalRelease](../vs140/CComPolyObject--FinalRelease.md)