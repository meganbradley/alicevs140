---
title: "CAtlFileMappingBase::Unmap"
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
ms.assetid: 8a22c535-f57b-4916-bbea-3a24c07bb08e
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CAtlFileMappingBase::Unmap
Call this method to unmap a file-mapping object.  
  
## Syntax  
  
```  
  
HRESULT Unmap( ) throw( );  
  
```  
  
## Return Value  
 Returns `S_OK` on success, or an error `HRESULT` on failure.  
  
## Remarks  
 See [UnmapViewOfFile](http://msdn.microsoft.com/library/windows/desktop/aa366882) in the [!INCLUDE[winSDK](../vs140/includes/winSDK_md.md)] for more details.  
  
## Requirements  
 **Header:** atlfile.h  
  
## See Also  
 [CAtlFileMappingBase Class](../vs140/CAtlFileMappingBase-Class.md)