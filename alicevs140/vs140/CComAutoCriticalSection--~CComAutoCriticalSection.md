---
title: "CComAutoCriticalSection::~CComAutoCriticalSection"
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
ms.assetid: 0930b19d-3b16-4dfd-892e-c002465d08e7
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CComAutoCriticalSection::~CComAutoCriticalSection
The destructor.  
  
## Syntax  
  
```  
  
~CComAutoCriticalSection( ) throw( );  
  
```  
  
## Remarks  
 The destructor calls [DeleteCriticalSection](http://msdn.microsoft.com/library/windows/desktop/ms682552), which releases all system resources used by the critical section object.  
  
## Requirements  
 **Header:** atlcore.h  
  
## See Also  
 [CComAutoCriticalSection Class](../vs140/CComAutoCriticalSection-Class.md)   
 [CComAutoCriticalSection::CComAutoCriticalSection](../vs140/CComAutoCriticalSection--CComAutoCriticalSection.md)