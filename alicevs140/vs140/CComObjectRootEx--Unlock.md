---
title: "CComObjectRootEx::Unlock"
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
ms.assetid: 05e82bdf-bb98-4178-a570-01485685454d
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CComObjectRootEx::Unlock
If the thread model is multithreaded, this method calls the Win32 API function [LeaveCriticalSection](http://msdn.microsoft.com/library/windows/desktop/ms684169), which releases ownership of the critical section object obtained through a private data member.  
  
## Syntax  
  
```  
  
void Unlock( );  
```  
  
## Remarks  
 To obtain ownership, the thread must call `Lock`. Each call to `Lock` requires a corresponding call to `Unlock` to release ownership of the critical section.  
  
 If the thread model is single-threaded, this method does nothing.  
  
## Requirements  
 **Header:** atlcom.h  
  
## See Also  
 [CComObjectRootEx Class](../vs140/CComObjectRootEx-Class.md)   
 [CComObjectRootEx::Lock](../vs140/CComObjectRootEx--Lock.md)