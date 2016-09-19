---
title: "basic_ostream::basic_ostream"
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
ms.assetid: aa09e4d4-26a0-4a06-9392-3bcd6865d457
caps.latest.revision: 20
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# basic_ostream::basic_ostream
Constructs a `basic_ostream` object.  
  
## Syntax  
  
```  
explicit basic_ostream(  
    basic_streambuf<_Elem, _Tr> *_Strbuf,  
    bool _Isstd = false  
);  
basic_ostream(  
    basic_ostream&& _Right  
);  
```  
  
#### Parameters  
 `_Strbuf`  
 An object of type [basic_streambuf](../vs140/basic_streambuf-Class.md).  
  
 `_Isstd`  
 `true` if this is a standard stream; otherwise, `false`.  
  
 `_Right`  
 An rvalue reference to an object of type `basic_ostream`.  
  
## Remarks  
 The first constructor initializes the base class by calling [init](../vs140/basic_ios--init.md)(`_Strbuf`). The second constructor initializes the base class by calling [move](../vs140/basic_ios--move.md)`(``_Right``)`.  
  
## Example  
 See the example for [basic_ofstream::basic_ofstream](../vs140/basic_ofstream--basic_ofstream.md) to learn more about output streams.  
  
## Requirements  
 **Header:** <ostream\>  
  
 **Namespace:** std  
  
## See Also  
 [basic_ostream Class](../vs140/basic_ostream-Class.md)   
 [iostream Programming](../vs140/iostream-Programming.md)   
 [iostreams Conventions](../vs140/iostreams-Conventions.md)