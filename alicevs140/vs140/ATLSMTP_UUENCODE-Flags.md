---
title: "ATLSMTP_UUENCODE Flags"
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
ms.assetid: ecb79b81-b764-4a48-a05c-a9dee6e7bbce
caps.latest.revision: 13
translation.priority.ht: 
  - de-de
  - ja-jp
---
# ATLSMTP_UUENCODE Flags
These flags describe how uuencoding is to be performed by [UUEncode](../vs140/UUEncode.md).  
  
## Syntax  
  
```  
  
      #define ATLSMTP_UUENCODE_HEADER   
#define ATLSMTP_UUENCODE_END   
#define ATLSMTP_UUENCODE_DOT  
```  
  
## Remarks  
  
|Flag|Description|  
|----------|-----------------|  
|ATLSMTP_UUENCODE_HEADER|The header will be encoded.|  
|ATLSMTP_UUENCODE_END|The end will be encoded.|  
|ATLSMTP_UUENCODE_DOT|Data stuffing will be performed.|  
  
## Requirements  
 **Header:** atlenc.h  
  
## See Also  
 [ATL Concepts](../vs140/Active-Template-Library--ATL--Concepts.md)   
 [ATL Reference](../vs140/ATL-COM-Desktop-Components.md)   
 [ATL Macros Alphabetical Reference](../vs140/ATL-Macros-Alphabetical-Reference.md)   
 [UUEncode](../vs140/UUEncode.md)