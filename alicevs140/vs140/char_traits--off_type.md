---
title: "char_traits::off_type"
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
ms.assetid: 8fe7f98c-c2fa-4e43-8aeb-11c97215c417
caps.latest.revision: 14
translation.priority.ht: 
  - de-de
  - ja-jp
---
# char_traits::off_type
An integer type that can represent offsets between positions in a stream.  
  
## Syntax  
  
```  
typedef streamoff off_type;  
```  
  
## Remarks  
 The type is a signed integer that describes an object that can store a byte offset involved in various stream positioning operations. It is typically a synonym for [streamoff](../vs140/streamoff.md), but it has essentially the same properties as that type.  
  
## Requirements  
 **Header:** <string\>  
  
 **Namespace:** std  
  
## See Also  
 [char_traits Struct](../vs140/char_traits-Struct.md)