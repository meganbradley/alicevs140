---
title: "CComAutoCriticalSection::CComAutoCriticalSection"
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
ms.assetid: 6bcf9aa9-1355-4c04-971e-75e9f2a37a40
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CComAutoCriticalSection::CComAutoCriticalSection
The constructor.  
  
## Syntax  
  
```  
  
CComAutoCriticalSection( );  
  
```  
  
## Remarks  
 Calls the Win32 function [InitializeCriticalSection](http://msdn.microsoft.com/library/windows/desktop/ms683472), which initializes the critical section object.  
  
## Requirements  
 **Header:** atlcore.h  
  
## See Also  
 [CComAutoCriticalSection Class](../vs140/CComAutoCriticalSection-Class.md)   
 [CComAutoCriticalSection::~CComAutoCriticalSection](../vs140/CComAutoCriticalSection--~CComAutoCriticalSection.md)