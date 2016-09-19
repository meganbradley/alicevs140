---
title: "CMultiLock::CMultiLock"
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
ms.assetid: 665fa4d9-256b-4b17-9493-e00b73e30d4e
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMultiLock::CMultiLock
Constructs a **CMultiLock** object.  
  
## Syntax  
  
```  
  
      CMultiLock(  
   CSyncObject* ppObjects[ ],  
   DWORD dwCount,  
   BOOL bInitialLock = FALSE   
);  
```  
  
#### Parameters  
 `ppObjects`  
 Array of pointers to the synchronization objects to be waited on. Cannot be **NULL**.  
  
 `dwCount`  
 Number of objects in `ppObjects`. Must be greater than 0.  
  
 `bInitialLock`  
 Specifies whether to initially attempt to access any of the supplied objects.  
  
## Remarks  
 This function is called after creating the array of synchronization objects to be waited on. It is usually called from within the thread that must wait for one of the synchronization objects to become available.  
  
## Requirements  
 **Header:** afxmt.h  
  
## See Also  
 [CMultiLock Class](../vs140/CMultiLock-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)