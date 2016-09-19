---
title: "CComCritSecLock::CComCritSecLock"
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
ms.assetid: 6bea525f-736c-4658-8e15-ced12ac83ac6
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CComCritSecLock::CComCritSecLock
The constructor.  
  
## Syntax  
  
```  
  
      CComCritSecLock(  
   TLock& cs,  
   bool bInitialLock = true   
);  
```  
  
#### Parameters  
 *cs*  
 The critical section object.  
  
 `bInitialLock`  
 The initial lock state: **true** means locked.  
  
## Remarks  
 Initializes the critical section object.  
  
## Requirements  
 **Header:** atlbase.h  
  
## See Also  
 [CComCritSecLock Class](../vs140/CComCritSecLock-Class.md)   
 [CComCritSecLock::~CComCritSecLock](../vs140/CComCritSecLock--~CComCritSecLock.md)