---
title: "ostream_iterator::ostream_type"
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
ms.assetid: 1b102a99-85bc-4ede-9c0c-b13e1c1fd819
caps.latest.revision: 15
translation.priority.ht: 
  - de-de
  - ja-jp
---
# ostream_iterator::ostream_type
A type that provides for the stream type of the iterator.  
  
## Syntax  
  
```  
typedef basic_ostream<CharType, Traits> ostream_type;  
```  
  
## Remarks  
 The type is a synonym for [basic_ostream](../vs140/basic_ostream-Class.md)<`CharType`, `Traits`>, a stream class of the iostream hierarchy that defines objects that can be used for writing.  
  
## Example  
 See [ostream_iterator](../vs140/ostream_iterator--ostream_iterator.md) for an example of how to declare and use `ostream_type`.  
  
## Requirements  
 **Header:** <iterator\>  
  
 **Namespace:** std  
  
## See Also  
 [ostream_iterator Class](../vs140/ostream_iterator-Class.md)   
 [Standard Template Library](../vs140/Standard-Template-Library.md)