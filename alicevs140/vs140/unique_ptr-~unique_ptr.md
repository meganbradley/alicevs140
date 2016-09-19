---
title: "unique_ptr ~unique_ptr"
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
ms.assetid: 2a52e757-7354-417a-932a-f837737ff19c
caps.latest.revision: 11
translation.priority.ht: 
  - de-de
  - ja-jp
---
# unique_ptr ~unique_ptr
The destructor for `unique_ptr`, destroys a `unique_ptr` object.  
  
## Syntax  
  
```  
~unique_ptr();  
```  
  
## Remarks  
 The destructor calls `get_deleter()(stored_ptr)`.  
  
## Requirements  
 **Header:** <memory\>  
  
 **Namespace:** std  
  
## See Also  
 [unique_ptr Class](../vs140/unique_ptr-Class.md)   
 [<memory\>](../vs140/-memory-.md)   
 [Thread Safety in the C++ Standard Library](../vs140/Thread-Safety-in-the-C---Standard-Library.md)