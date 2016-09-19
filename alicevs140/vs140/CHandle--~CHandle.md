---
title: "CHandle::~CHandle"
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
ms.assetid: 5535e750-ca9f-411f-94df-9dea4cc12213
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CHandle::~CHandle
The destructor.  
  
## Syntax  
  
```  
  
~CHandle( ) throw( );  
  
```  
  
## Remarks  
 Frees the `CHandle` object by calling [CHandle::Close](../vs140/CHandle--Close.md).  
  
## Requirements  
 **Header:** atlbase.h  
  
## See Also  
 [CHandle Class](../vs140/CHandle-Class.md)   
 [CHandle::CHandle](../vs140/CHandle--CHandle.md)