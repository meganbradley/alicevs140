---
title: "CComObjectRootEx::Lock"
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
ms.assetid: 5aaa0871-8c0c-43b1-bc8f-e9d6d51b654d
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CComObjectRootEx::Lock
If the thread model is multithreaded, this method calls the Win32 API function [EnterCriticalSection](http://msdn.microsoft.com/library/windows/desktop/ms682608), which waits until the thread can take ownership of the critical section object obtained through a private data member.  
  
## Syntax  
  
```  
  
void Lock( );  
```  
  
## Remarks  
 When the protected code finishes executing, the thread must call `Unlock` to release ownership of the critical section.  
  
 If the thread model is single-threaded, this method does nothing.  
  
## Requirements  
 **Header:** atlcom.h  
  
## See Also  
 [CComObjectRootEx Class](../vs140/CComObjectRootEx-Class.md)   
 [CComObjectRootEx::Unlock](../vs140/CComObjectRootEx--Unlock.md)