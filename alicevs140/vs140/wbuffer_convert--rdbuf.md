---
title: "wbuffer_convert::rdbuf"
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
ms.topic: article
ms.assetid: 56ea5363-65a7-4b84-b590-534e4b460c29
caps.latest.revision: 13
translation.priority.ht: 
  - de-de
  - ja-jp
---
# wbuffer_convert::rdbuf
Returns the byte stream buffer.  
  
## Syntax  
  
```  
std::streambuf *rdbuf() const;  
std::streambuf *rdbuf(std::streambuf *_Bytebuf);  
```  
  
#### Parameters  
  
|Parameter|Description|  
|---------------|-----------------|  
|`*_Bytebuf`|The byte stream buffer to be stored in the object representing the byte stream buffer.|  
  
## Return Value  
 An object representing the underlying byte stream buffer.  
  
## Remarks  
 The second member function stores `_Bytebuf` in the object representing the byte stream buffer.  
  
## Requirements  
 **Header:** <locale\>  
  
 **Namespace:** std  
  
## See Also  
 [wbuffer_convert Class](../vs140/wbuffer_convert-Class.md)