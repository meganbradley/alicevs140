---
title: "CHandle::CHandle"
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
ms.assetid: 5332e35e-0265-4e9e-a0a6-5bf7d5f12ce8
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CHandle::CHandle
The constructor.  
  
## Syntax  
  
```  
  
      CHandle( ) throw( );   
CHandle(  
   CHandle& h   
) throw( );  
explicit CHandle(  
   HANDLE h   
) throw( );  
```  
  
#### Parameters  
 `h`  
 An existing handle or `CHandle`.  
  
## Remarks  
 Creates a new `CHandle` object, optionally using an existing handle or `CHandle` object.  
  
## Requirements  
 **Header:** atlbase.h  
  
## See Also  
 [CHandle Class](../vs140/CHandle-Class.md)   
 [CHandle::Attach](../vs140/CHandle--Attach.md)