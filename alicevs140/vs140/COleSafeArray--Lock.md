---
title: "COleSafeArray::Lock"
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
ms.assetid: 599fbbf3-5119-444b-948a-4d13c0df92f4
caps.latest.revision: 15
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# COleSafeArray::Lock
Increments the lock count of an array and place a pointer to the array data in the array descriptor.  
  
## Syntax  
  
```  
  
void Lock( );  
```  
  
## Remarks  
 On error, it throws a [COleException](../vs140/COleException-Class.md).  
  
 The pointer in the array descriptor is valid until `Unlock` is called. Calls to `Lock` can be nested; an equal number of calls to `Unlock` are required.  
  
 An array cannot be deleted while it is locked.  
  
## Requirements  
 **Header:** afxdisp.h  
  
## See Also  
 [COleSafeArray Class](../vs140/COleSafeArray-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [COleSafeArray::Unlock](../vs140/COleSafeArray--Unlock.md)