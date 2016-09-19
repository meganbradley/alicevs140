---
title: "CMFCFilterChunkValueImpl::SetSystemTimeValue"
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
ms.assetid: 8bd7fecf-9199-4ccd-b270-0df2a206d270
caps.latest.revision: 10
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMFCFilterChunkValueImpl::SetSystemTimeValue
Sets the property by key to a SystemTime.  
  
## Syntax  
  
```  
HRESULT SetSystemTimeValue(  
   REFPROPERTYKEY pkey,  
   const SYSTEMTIME &systemTime,  
   CHUNKSTATE chunkType = CHUNK_VALUE,  
   LCID locale=0,  
   DWORD cwcLenSource=0,  
   DWORD cwcStartSource=0,  
   CHUNK_BREAKTYPE chunkBreakType=CHUNK_NO_BREAK  
);  
```  
  
#### Parameters  
 `pkey`  
 Specifies a property key.  
  
 `systemTime`  
 Specifies the chunk value to set.  
  
 `chunkType`  
 Flags indicate whether this chunk contains a text-type or a value-type property. Flag values are taken from the CHUNKSTATE enumeration.  
  
 `locale`  
 The language and sublanguage associated with a chunk of text. Chunk locale is used by document indexers to perform proper word breaking of text. If the chunk is neither text-type nor a value-type with data type VT_LPWSTR, VT_LPSTR, or VT_BSTR, this field is ignored.  
  
 `cwcLenSource`  
 The length in characters of the source text from which the current chunk was derived. A zero value signifies character-by-character correspondence between the source text and the derived text. A nonzero value means that no such direct correspondence exists.  
  
 `cwcStartSource`  
 The offset from which the source text for a derived chunk starts in the source chunk.  
  
 `chunkBreakType`  
 The type of break that separates the previous chunk from the current chunk. Values are from the CHUNK_BREAKTYPE enumeration.  
  
## Return Value  
 S_OK if successful; otherwise an error code.  
  
## Remarks  
  
## Requirements  
 **Header:** afxwin.h  
  
## See Also  
 [CMFCFilterChunkValueImpl Class](../vs140/CMFCFilterChunkValueImpl-Class.md)