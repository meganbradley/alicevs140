---
title: "CAtlTemporaryFile::HandsOff"
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
ms.assetid: 12254237-40e7-4910-bce4-968bea32d157
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CAtlTemporaryFile::HandsOff
Call this method to disassociate the file from the `CAtlTemporaryFile` object.  
  
## Syntax  
  
```  
  
HRESULT HandsOff( ) throw( );  
  
```  
  
## Return Value  
 Returns `S_OK` on success, or an error `HRESULT` on failure.  
  
## Remarks  
 `HandsOff` and [CAtlTemporaryFile::HandsOn](../vs140/CAtlTemporaryFile--HandsOn.md) are used to disassociate the file from the object, and reattach it if needed. `HandsOff` will force any data remaining in the file buffer to be written to the temporary file, and then close the file. If you want to close and delete the file permanently, or if you want to close and retain the contents of the file with a given name, use [CAtlTemporaryFile::Close](../vs140/CAtlTemporaryFile--Close.md).  
  
## Requirements  
 **Header:** atlfile.h  
  
## See Also  
 [CAtlTemporaryFile Class](../vs140/CAtlTemporaryFile-Class.md)   
 [CAtlTemporaryFile::HandsOn](../vs140/CAtlTemporaryFile--HandsOn.md)