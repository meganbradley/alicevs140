---
title: "CAtlTemporaryFile::HandsOn"
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
ms.assetid: 7e64502d-b65b-48fb-8cc3-330d0eade67c
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CAtlTemporaryFile::HandsOn
Call this method to open an existing temporary file and position the pointer at the end of the file.  
  
## Syntax  
  
```  
  
HRESULT HandsOn( ) throw( );  
  
```  
  
## Return Value  
 Returns `S_OK` on success, or an error `HRESULT` on failure.  
  
## Remarks  
 [CAtlTemporaryFile::HandsOff](../vs140/CAtlTemporaryFile--HandsOff.md) and `HandsOn` are used to disassociate the file from the object, and reattach it if needed.  
  
## Requirements  
 **Header:** atlfile.h  
  
## See Also  
 [CAtlTemporaryFile Class](../vs140/CAtlTemporaryFile-Class.md)   
 [CAtlTemporaryFile::HandsOff](../vs140/CAtlTemporaryFile--HandsOff.md)