---
title: "ATLSMTP_QPENCODE Flags"
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
ms.assetid: 6b15a3ab-8e57-49e4-8104-09b26ebb96c4
caps.latest.revision: 16
translation.priority.ht: 
  - de-de
  - ja-jp
---
# ATLSMTP_QPENCODE Flags
These flags describe how quoted-printable encoding is to be performed by [QPEncode](../vs140/QPEncode.md).  
  
## Syntax  
  
```  
  
      #define ATLSMTP_QPENCODE_DOT   
#define ATLSMTP_QPENCODE_TRAILING_SOFT  
```  
  
## Remarks  
  
|Flag|Description|  
|----------|-----------------|  
|ATLSMTP_QPENCODE_DOT|If a period appears at the start of a line, it is added to the output as well as encoded.|  
|ATLSMTP_QPENCODE_TRAILING_SOFT|Appends =\r\n to the encoded string.|  
  
 The quoted-printable encoding scheme is described in RFC 2045 ([http://www.ietf.org/rfc/rfc2045.txt](http://www.ietf.org/rfc/rfc2045.txt)).  
  
## Requirements  
 **Header:** atlenc.h  
  
## See Also  
 [ATL Concepts](../vs140/Active-Template-Library--ATL--Concepts.md)   
 [ATL Reference](../vs140/ATL-COM-Desktop-Components.md)   
 [ATL Macros Alphabetical Reference](../vs140/ATL-Macros-Alphabetical-Reference.md)   
 [QPEncode](../vs140/QPEncode.md)