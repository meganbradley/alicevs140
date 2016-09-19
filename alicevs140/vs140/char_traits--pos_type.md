---
title: "char_traits::pos_type"
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
ms.assetid: 8110e488-3b9a-4dc4-8c76-0c06791e9d36
caps.latest.revision: 14
translation.priority.ht: 
  - de-de
  - ja-jp
---
# char_traits::pos_type
An integer type that can represent positions in a stream.  
  
## Syntax  
  
```  
typedef streampos pos_type;  
```  
  
## Remarks  
 The type describes an object that can store all the information needed to restore an arbitrary file-position indicator within a stream. It is typically a synonym for [streampos](../vs140/streampos.md), but in any case it has essentially the same properties as that type.  
  
## Requirements  
 **Header:** <string\>  
  
 **Namespace:** std  
  
## See Also  
 [char_traits Struct](../vs140/char_traits-Struct.md)