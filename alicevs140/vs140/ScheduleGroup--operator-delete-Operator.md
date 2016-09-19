---
title: "ScheduleGroup::operator delete Operator"
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
ms.assetid: 8281e36e-568c-4b3d-9c52-600e48737a47
caps.latest.revision: 17
translation.priority.ht: 
  - de-de
  - ja-jp
---
# ScheduleGroup::operator delete Operator
A `ScheduleGroup` object is destroyed internally by the runtime when all external references to it are released. It cannot be explicitly deleted.  
  
## Syntax  
  
```  
void operator delete(  
   void * _PObject  
);  
  
void operator delete(  
   void * _PObject,  
   int,  
   const char *,  
   int  
);  
```  
  
#### Parameters  
 `_PObject`  
 A pointer to the object to be deleted.  
  
## Requirements  
 **Header:** concrt.h  
  
 **Namespace:** concurrency  
  
## See Also  
 [ScheduleGroup Class](../vs140/ScheduleGroup-Class.md)