---
title: "CriticalSection::CriticalSection Constructor"
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
ms.assetid: 930b89be-4d74-46bd-8879-5dd4d15bcbd0
caps.latest.revision: 5
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CriticalSection::CriticalSection Constructor
Initializes a synchronization object that is similar to a mutex object, but can be used by only the threads of a single process.  
  
## Syntax  
  
```  
explicit CriticalSection(  
   ULONG spincount = 0  
);  
```  
  
#### Parameters  
 `spincount`  
 The spin count for the critical section object. The default value is 0.  
  
## Remarks  
 For more information about crticial sections and spincounts, see the **InitializeCriticalSectionAndSpinCount** function in the Synchronization section of the Windows API documenation.  
  
## Requirements  
 **Header:** corewrappers.h  
  
 **Namespace:** Microsoft::WRL::Wrappers  
  
## See Also  
 [CriticalSection Class](../vs140/CriticalSection-Class.md)