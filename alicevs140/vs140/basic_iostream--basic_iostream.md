---
title: "basic_iostream::basic_iostream"
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
ms.assetid: 29faed2b-5a5c-468a-abdc-ca4429847fd4
caps.latest.revision: 11
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# basic_iostream::basic_iostream
Create a `basic_iostream` object.  
  
## Syntax  
  
```  
explicit basic_iostream(basic_streambuf<Elem, Tr> *_Strbuf);  
basic_iostream(basic_iostream&& _Right);  
basic_iostream();  
```  
  
#### Parameters  
 `_Strbuf`  
 An existing `basic_streambuf` object.  
  
 `_Right`  
 An existing `basic_iostream` object that is used to construct a new `basic_iostream`.  
  
## Property Value/Return Value  
  
## Exceptions  
  
## Remarks  
 The first constructor initializes the base objects by way of `basic_istream(``_Strbuf``)` and `basic_ostream(``_Strbuf``)`.  
  
 The second constructor initializes the base objects by calling `(``_Right``)`.  
  
## Requirements  
 **Header:** <istream\>  
  
 **Namespace:** std  
  
## Subhead  
  
## See Also  
 [basic_iostream Class](../vs140/basic_iostream-Class.md)   
 [<istream\>](../vs140/-istream-.md)   
 [lvalues and rvalues](../vs140/Lvalues-and-Rvalues--Visual-C---.md)