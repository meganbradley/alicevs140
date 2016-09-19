---
title: "CMFCFilterChunkValueImpl::CopyChunk"
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
ms.assetid: 002d4eaf-cbfe-46e0-baef-2c62859f1cd2
caps.latest.revision: 10
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMFCFilterChunkValueImpl::CopyChunk
Copies this chunk to a structure describing the characteristics of a chunk.  
  
## Syntax  
  
```  
HRESULT CopyChunk(  
   STAT_CHUNK *pStatChunk  
);  
```  
  
#### Parameters  
 `pStatChunk`  
 A pointer to destination value describing the characteristics of the chunk.  
  
## Return Value  
 S_OK if successful; otherwise an error code.  
  
## Remarks  
  
## Requirements  
 **Header:** afxwin.h  
  
## See Also  
 [CMFCFilterChunkValueImpl Class](../vs140/CMFCFilterChunkValueImpl-Class.md)