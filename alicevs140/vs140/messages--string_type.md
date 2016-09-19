---
title: "messages::string_type"
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
ms.assetid: 0de8b10b-a85c-425e-bdcc-02240d47aa1e
caps.latest.revision: 14
translation.priority.ht: 
  - de-de
  - ja-jp
---
# messages::string_type
A type that describes a string of type `basic_string` containing characters of type **CharType**.  
  
## Syntax  
  
```  
typedef basic_string<CharType, Traits, Allocator> string_type;  
```  
  
## Remarks  
 The type describes a specialization of template class [basic_string](../vs140/basic_string-Class.md) whose objects can store copies of the message sequences.  
  
## Requirements  
 **Header:** <locale\>  
  
 **Namespace:** std  
  
## See Also  
 [messages Class](../vs140/messages-Class.md)