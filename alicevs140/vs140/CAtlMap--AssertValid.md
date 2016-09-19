---
title: "CAtlMap::AssertValid"
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
ms.assetid: 5f5d251d-6b50-4519-807f-86b128be7b8a
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CAtlMap::AssertValid
Call this method to cause an ASSERT if the `CAtlMap` object is not valid.  
  
## Syntax  
  
```  
  
void AssertValid( ) const;  
  
```  
  
## Remarks  
 In debug builds, this method will cause an ASSERT if the `CAtlMap` object is not valid.  
  
## Example  
 See the example for [CAtlMap::CAtlMap](../vs140/CAtlMap--CAtlMap.md).  
  
## Requirements  
 **Header:** atlcoll.h  
  
## See Also  
 [CAtlMap Class](../vs140/CAtlMap-Class.md)   
 [CAtlMap::IsEmpty](../vs140/CAtlMap--IsEmpty.md)