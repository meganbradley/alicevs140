---
title: "basic_streambuf::swap"
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
ms.assetid: 4834ab5e-eeb1-421c-a40f-893ed77a1501
caps.latest.revision: 15
translation.priority.ht: 
  - de-de
  - ja-jp
---
# basic_streambuf::swap
Exchanges the values in this object for the values in the provided `basic_streambuf` object.  
  
## Syntax  
  
```  
void swap(  
    basic_streambuf& _Right  
);  
```  
  
#### Parameters  
  
|Parameter|Description|  
|---------------|-----------------|  
|`_Right`|An lvalue reference to the `basic_streambuf` object that is used to exchange values.|  
  
## Remarks  
 The protected member function exchanges with `_Right` all the pointers controlling the `input buffer` and the `output buffer`. It also exchanges `_Right``.`[getloc()](../vs140/basic_streambuf--getloc.md) with the `locale` object.  
  
## Requirements  
 **Header:** <streambuf\>  
  
 **Namespace:** std  
  
## See Also  
 [basic_streambuf Class](../vs140/basic_streambuf-Class.md)   
 [<streambuf\>](../vs140/-streambuf-.md)   
 [lvalues and rvalues](../vs140/Lvalues-and-Rvalues--Visual-C---.md)   
 [iostream Programming](../vs140/iostream-Programming.md)   
 [iostreams Conventions](../vs140/iostreams-Conventions.md)