---
title: "CStringData::Unlock"
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
ms.assetid: ec1c9289-0f1c-4e5e-a14c-7076c4e3ea40
caps.latest.revision: 11
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CStringData::Unlock
Unlocks the character buffer of the associated string object.  
  
## Syntax  
  
```  
  
void Unlock( ) throw( );  
  
```  
  
## Remarks  
 Call this function to unlock the character buffer of the string data object. Once a buffer is unlocked, it is shareable and can be reference counted.  
  
> [!NOTE]
>  Each call to `Lock` must be matched by a corresponding call to `Unlock`.  
  
 Locking and unlocking is used when the developer must ensure that the string data not be shared. A good example of locking is demonstrated by the [LockBuffer](../vs140/CSimpleStringT--LockBuffer.md) and [UnlockBuffer](../vs140/CSimpleStringT--UnlockBuffer.md) methods of `CSimpleStringT`.  
  
## Requirements  
 **Header:** atlsimpstr.h  
  
## See Also  
 [CStringData Class](../vs140/CStringData-Class.md)   
 [CStringData::Lock](../vs140/CStringData--Lock.md)