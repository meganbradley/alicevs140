---
title: "CAtlFileMapping::operator T*"
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
ms.assetid: 80a7b12c-1f9a-4c25-a7d7-c7c088a2f2f9
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CAtlFileMapping::operator T*
Allows implicit conversion of `CAtlFileMapping` objects to `T`**\***.  
  
## Syntax  
  
```  
  
operator T*() const throw( );  
  
```  
  
## Return Value  
 Returns a `T`**\*** pointer to the start of the memory-mapped file.  
  
## Remarks  
 Calls [CAtlFileMappingBase::GetData](../vs140/CAtlFileMappingBase--GetData.md) and reinterprets the returned pointer as a `T`**\*** where *T* is the type used as the template parameter of this class.  
  
## Requirements  
 **Header:** atlfile.h  
  
## See Also  
 [CAtlFileMappingBase Class](../vs140/CAtlFileMappingBase-Class.md)   
 [CAtlFileMappingBase::GetData](../vs140/CAtlFileMappingBase--GetData.md)