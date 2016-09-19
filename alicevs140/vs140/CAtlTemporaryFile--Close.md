---
title: "CAtlTemporaryFile::Close"
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
ms.assetid: dec76396-da76-4be0-8cb8-ed8ad4a17ff8
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CAtlTemporaryFile::Close
Call this method to close a temporary file and either delete its contents or store them under the specified file name.  
  
## Syntax  
  
```  
  
      HRESULT Close(  
   LPCTSTR szNewName = NULL   
) throw( );  
```  
  
#### Parameters  
 *szNewName*  
 The name for the new file to store the contents of the temporary file in. If this argument is NULL, the contents of the temporary file are deleted.  
  
## Return Value  
 Returns `S_OK` on success, or an error `HRESULT` on failure.  
  
## Example  
 See the example for [CAtlTemporaryFile::CAtlTemporaryFile](../vs140/CAtlTemporaryFile--CAtlTemporaryFile.md).  
  
## Requirements  
 **Header:** atlfile.h  
  
## See Also  
 [CAtlTemporaryFile Class](../vs140/CAtlTemporaryFile-Class.md)   
 [CAtlTemporaryFile::HandsOff](../vs140/CAtlTemporaryFile--HandsOff.md)   
 [CAtlTemporaryFile::Create](../vs140/CAtlTemporaryFile--Create.md)