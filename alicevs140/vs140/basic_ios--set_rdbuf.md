---
title: "basic_ios::set_rdbuf"
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
ms.assetid: 6171b861-7be9-4e33-9804-374b5461bad3
caps.latest.revision: 11
translation.priority.mt: 
  - de-de
  - ja-jp
---
# basic_ios::set_rdbuf
Assigns a stream buffer to be the read buffer for this stream object.  
  
## Syntax  
  
```  
void set_rdbuf(  
    basic_streambuf<Elem, Tr> *_Strbuf  
)  
```  
  
#### Parameters  
 `_Strbuf`  
 The stream buffer to become the read buffer.  
  
## Property Value/Return Value  
  
## Remarks  
 The protected member function stores `_Strbuf` in the `stream buffer pointer`.It does not call `clear`.  
  
## Requirements  
 **Header:** <ios\>  
  
 **Namespace:** std  
  
## See Also  
 [basic_ios Class](../vs140/basic_ios-Class.md)   
 [iostream Programming](../vs140/iostream-Programming.md)   
 [iostreams Conventions](../vs140/iostreams-Conventions.md)