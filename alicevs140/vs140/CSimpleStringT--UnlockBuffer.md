---
title: "CSimpleStringT::UnlockBuffer"
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
ms.assetid: 45ed73e4-6d5d-45fc-80e1-f4be2475aa17
caps.latest.revision: 11
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CSimpleStringT::UnlockBuffer
Unlocks the buffer of the `CSimpleStringT` object.  
  
## Syntax  
  
```  
  
void UnlockBuffer( ) throw( );  
  
```  
  
## Remarks  
 Call this method to reset the reference count of the string to 1.  
  
 The `CSimpleStringT` destructor automatically calls `UnlockBuffer` to ensure that the buffer is not locked when the destructor is called. For an example of this method, see [LockBuffer](../vs140/CSimpleStringT--LockBuffer.md).  
  
## Requirements  
 **Header:** atlsimpstr.h  
  
## See Also  
 [CSimpleStringT Class](../vs140/CSimpleStringT-Class.md)   
 [CSimpleStringT::LockBuffer](../vs140/CSimpleStringT--LockBuffer.md)   
 [CSimpleStringT::GetBuffer](../vs140/CSimpleStringT--GetBuffer.md)   
 [CSimpleStringT::ReleaseBuffer](../vs140/CSimpleStringT--ReleaseBuffer.md)