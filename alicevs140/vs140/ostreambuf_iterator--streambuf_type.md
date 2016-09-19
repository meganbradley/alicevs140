---
title: "ostreambuf_iterator::streambuf_type"
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
ms.assetid: 8c6cb6a8-de60-4269-ab03-bc772ffb01a3
caps.latest.revision: 14
translation.priority.ht: 
  - de-de
  - ja-jp
---
# ostreambuf_iterator::streambuf_type
A type that provides for the stream type of the `ostreambuf_iterator`.  
  
## Syntax  
  
```  
  
typedef basic_streambuf<CharType, Traits> streambuf_type;  
  
```  
  
## Remarks  
 The type is a synonym for `basic_streambuf`<**CharType**, **Traits**>, a stream class for I/O buffers that becomes `streambuf` when specialized to character type `char`.  
  
## Example  
 See [ostreambuf_iterator](../vs140/ostreambuf_iterator--ostreambuf_iterator.md) for an example of how to declare and use `streambuf_type`.  
  
## Requirements  
 **Header:** <iterator\>  
  
 **Namespace:** std  
  
## See Also  
 [ostreambuf_iterator Class](../vs140/ostreambuf_iterator-Class.md)   
 [Standard Template Library](../vs140/Standard-Template-Library.md)