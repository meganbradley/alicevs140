---
title: "CAtlFile::CAtlFile"
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
ms.assetid: 02aa72e8-cbd1-42a2-974e-59af43e08a5f
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CAtlFile::CAtlFile
The constructor.  
  
## Syntax  
  
```  
  
      CAtlFile( ) throw( );   
CAtlFile(  
   CAtlTransactionManager* pTM = NULL  
) throw( );  
CAtlFile(  
   CAtlFile& file   
) throw( );  
explicit CAtlFile(  
   HANDLE hFile   
) throw( );  
```  
  
#### Parameters  
 `file`  
 The file object.  
  
 `hFile`  
 The file handle.  
  
 `pTM`  
 Pointer to CAtlTransactionManager object  
  
## Remarks  
 The copy constructor transfers ownership of the file handle from the original `CAtlFile` object to the newly constructed object.  
  
## Requirements  
 **Header:** atlfile.h  
  
## See Also  
 [CAtlFile Class](../vs140/CAtlFile-Class.md)