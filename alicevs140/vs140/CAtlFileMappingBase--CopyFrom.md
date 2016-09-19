---
title: "CAtlFileMappingBase::CopyFrom"
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
ms.assetid: 8b13baf6-d194-430b-8173-67f9f63d78c5
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CAtlFileMappingBase::CopyFrom
Call this method to copy from a file-mapping object.  
  
## Syntax  
  
```  
  
      HRESULT CopyFrom(  
   CAtlFileMappingBase& orig   
) throw( );  
```  
  
#### Parameters  
 `orig`  
 The original file-mapping object to copy from.  
  
## Return Value  
 Returns `S_OK` on success, or an error `HRESULT` on failure.  
  
## Requirements  
 **Header:** atlfile.h  
  
## See Also  
 [CAtlFileMappingBase Class](../vs140/CAtlFileMappingBase-Class.md)