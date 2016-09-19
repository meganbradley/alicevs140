---
title: "char_traits::state_type"
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
ms.assetid: f0b83473-5026-40ce-8f6c-5470cdb112de
caps.latest.revision: 13
translation.priority.ht: 
  - de-de
  - ja-jp
---
# char_traits::state_type
A type that represents the conversion state for multibyte characters in a stream.  
  
## Syntax  
  
```  
  
typedef implementation-defined state_type;  
```  
  
## Remarks  
 The type describes an object that can represent a conversion state. It is typically a synonym for `mbstate_t`, but in any case it has essentially the same properties as that type.  
  
## Requirements  
 **Header:** <string\>  
  
 **Namespace:** std  
  
## See Also  
 [char_traits Struct](../vs140/char_traits-Struct.md)