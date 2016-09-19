---
title: "basic_ios::swap"
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
ms.assetid: c90e49d1-d9d1-435b-b17f-100806c4aeff
caps.latest.revision: 11
translation.priority.ht: 
  - de-de
  - ja-jp
---
# basic_ios::swap
Exchanges the values in this `basic_ios` object for those of another `basic_ios` object. However, the pointers to the stream buffers are not swapped.  
  
## Syntax  
  
```  
void swap(basic_ios&& _Right);  
```  
  
#### Parameters  
 `_Right`  
 The `basic_ios` object that is used to exchange values.  
  
## Remarks  
 The protected member function exchanges all the values stored in `_Right` with `*this` except the stored `stream buffer pointer`.  
  
## Requirements  
 **Header:** <ios\>  
  
 **Namespace:** std  
  
## See Also  
 [basic_ios Class](../vs140/basic_ios-Class.md)   
 [lvalues and rvalues](../vs140/Lvalues-and-Rvalues--Visual-C---.md)   
 [iostream Programming](../vs140/iostream-Programming.md)   
 [iostreams Conventions](../vs140/iostreams-Conventions.md)