---
title: "ATL_URL Flags"
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
ms.assetid: 76e8cc5c-4e17-4eb1-ac29-a94d5256c4a7
caps.latest.revision: 14
translation.priority.ht: 
  - de-de
  - ja-jp
---
# ATL_URL Flags
These flags modify the behavior of [AtlEscapeUrl](../vs140/AtlEscapeUrl.md) and [AtlCanonicalizeUrl](../vs140/AtlCanonicalizeUrl.md) .  
  
## Syntax  
  
```  
  
      #define ATL_URL_ESCAPE   
#define ATL_URL_NO_ENCODE   
#define ATL_URL_DECODE   
#define ATL_URL_NO_META   
#define ATL_URL_ENCODE_SPACES_ONLY   
#define ATL_URL_BROWSER_MODE   
#define ATL_URL_ENCODE_PERCENT  
```  
  
## Remarks  
  
|Flag|Description|  
|----------|-----------------|  
|ATL_URL_BROWSER_MODE|Does not encode or decode characters after "#" or "?", and does not remove trailing white space after "?". If this value is not specified, the entire URL is encoded and trailing white space is removed.|  
|ATL_URL_DECODE|Converts all %XX sequences to characters, including escape sequences, before the URL is parsed.|  
|ATL_URL_ENCODE_PERCENT|Encodes any percent signs encountered. By default, percent signs are not encoded.|  
|ATL_URL_ENCODE_SPACES_ONLY|Encodes spaces only.|  
|ATL_URL_ESCAPE|Converts all escape sequences (%XX) to their corresponding characters.|  
|ATL_URL_NO_ENCODE|Does not convert unsafe characters to escape sequences.|  
|ATL_URL_NO_META|Does not remove meta sequences (such as "." and "..") from the URL.|  
  
## Requirements  
 **Header:** atlutil.h  
  
## See Also  
 [ATL Concepts](../vs140/Active-Template-Library--ATL--Concepts.md)   
 [ATL Reference](../vs140/ATL-COM-Desktop-Components.md)   
 [ATL Macros Alphabetical Reference](../vs140/ATL-Macros-Alphabetical-Reference.md)