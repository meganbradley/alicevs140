---
title: "basic_streambuf::sync"
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
ms.assetid: 2d4d5e69-cc0e-421c-960a-c37a383c138a
caps.latest.revision: 15
translation.priority.ht: 
  - de-de
  - ja-jp
---
# basic_streambuf::sync
A protected virtual function that tries to synchronize the controlled streams with any associated external streams.  
  
## Syntax  
  
```  
  
virtual int sync( );  
  
```  
  
## Return Value  
 If the function cannot succeed, it returns -1. The default behavior is to return zero.  
  
## Remarks  
 `sync` involves writing out any elements between the beginning and next pointers for the output buffer. It does not involve putting back any elements between the next and end pointers for the input buffer.  
  
## Requirements  
 **Header:** <streambuf\>  
  
 **Namespace:** std  
  
## See Also  
 [basic_streambuf Class](../vs140/basic_streambuf-Class.md)   
 [iostream Programming](../vs140/iostream-Programming.md)   
 [iostreams Conventions](../vs140/iostreams-Conventions.md)