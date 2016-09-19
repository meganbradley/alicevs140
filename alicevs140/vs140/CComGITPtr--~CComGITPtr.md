---
title: "CComGITPtr::~CComGITPtr"
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
ms.assetid: 272c818d-4d89-4107-a0af-fc0a93780a26
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CComGITPtr::~CComGITPtr
The destructor.  
  
## Syntax  
  
```  
  
~CComGITPtr( ) throw( );  
  
```  
  
## Remarks  
 Removes the interface from the global interface table (GIT), using [CComGITPtr::Revoke](../vs140/CComGITPtr--Revoke.md).  
  
## Requirements  
 **Header:** atlbase.h  
  
## See Also  
 [CComGITPtr Class](../vs140/CComGITPtr-Class.md)