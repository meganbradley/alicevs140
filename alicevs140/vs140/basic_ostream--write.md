---
title: "basic_ostream::write"
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
ms.assetid: 673f9510-ea4d-4037-887d-0c3e3358c30e
caps.latest.revision: 17
robots: noindex,nofollow
translation.priority.mt: 
  - de-de
  - ja-jp
---
# basic_ostream::write
Put characters in a stream.  
  
## Syntax  
  
```  
basic_ostream<_Elem, _Tr>& write(  
    const char_type *_Str,  
    streamsize _Count  
);  
```  
  
#### Parameters  
 `_Count`  
 Count of characters to put into the stream.  
  
 `_Str`  
 Characters to put into the stream.  
  
## Return Value  
 A reference to the basic_ostream object.  
  
## Remarks  
 The [unformatted output function](../vs140/basic_ostream-Class.md) inserts the sequence of `_Count` elements beginning at `_Str`.  
  
## Example  
 See [streamsize](../vs140/streamsize.md) for an example using `write`.  
  
## Requirements  
 **Header:** <ostream\>  
  
 **Namespace:** std  
  
## See Also  
 [basic_ostream Class](../vs140/basic_ostream-Class.md)   
 [iostream Programming](../vs140/iostream-Programming.md)   
 [iostreams Conventions](../vs140/iostreams-Conventions.md)