---
title: "CDocument::FindChunk"
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
ms.assetid: a66ebbdb-e22d-4cd7-b601-b1d1407e658c
caps.latest.revision: 11
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CDocument::FindChunk
Looks for a chunk with a specified GUID.  
  
## Syntax  
  
```  
virtual POSITION FindChunk(  
   REFCLSID guid,  
   DWORD pid  
);  
```  
  
#### Parameters  
 `guid`  
 Specifies the GUID of a chunk to find.  
  
 `pid`  
 Specifies a PID of a chunk to find.  
  
## Return Value  
 Position in the internal chunk list if successful. Otherwise `NULL`.  
  
## Remarks  
  
## Requirements  
 **Header:** afxwin.h  
  
## See Also  
 [CDocument Class](../vs140/CDocument-Class.md)