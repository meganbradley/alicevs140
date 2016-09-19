---
title: "CDocument::RemoveChunk"
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
ms.assetid: 8260da2a-4cea-44d6-99b4-37db0eb5c568
caps.latest.revision: 11
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CDocument::RemoveChunk
Removes a chunk with the specified GUID.  
  
## Syntax  
  
```  
virtual void RemoveChunk(  
   REFCLSID guid,  
   DWORD pid  
);  
```  
  
#### Parameters  
 `Guid`  
 Specifies the GUID of a chunk to be removed.  
  
 `Pid`  
 Specifies the PID of a chunk to be removed.  
  
## Remarks  
  
## Requirements  
 **Header:** afxwin.h  
  
## See Also  
 [CDocument Class](../vs140/CDocument-Class.md)