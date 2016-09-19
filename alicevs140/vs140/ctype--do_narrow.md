---
title: "ctype::do_narrow"
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
ms.assetid: 30f5a29d-064f-45d3-9996-97d56951f5a8
caps.latest.revision: 20
translation.priority.ht: 
  - de-de
  - ja-jp
---
# ctype::do_narrow
A virtual function called to convert a character of type `CharType` used by a locale to the corresponding character of type `char` in the native character set.  
  
## Syntax  
  
```  
virtual char do_narrow(  
    CharType ch,   
    char default = '\0'  
) const;  
virtual const CharType* do_narrow(  
    const CharType* first,   
    const CharType* last,  
    char default,   
    char* dest  
) const;  
```  
  
#### Parameters  
 `ch`  
 The character of type `Chartype` used by the locale to be converted.  
  
 `default`  
 The default value to be assigned by the member function to characters of type `CharType` that do not have counterpart characters of type `char`.  
  
 `first`  
 A pointer to the first character in the range of characters to be converted.  
  
 `last`  
 A pointer to the character immediately following the last character in the range of characters to be converted.  
  
 `dest`  
 A const pointer to the first character of type `char` in the destination range that stores the converted range of characters.  
  
## Return Value  
 The first protected member function returns the native character of type char that corresponds to the parameter character of type `CharType` or `default` if no counterpart is defined.  
  
 The second protected member function returns a pointer to the destination range of native characters converted from characters of type `CharType`.  
  
## Remarks  
 The second protected member template function stores in `dest`[`I`] the value `do_narrow`(`first` [`I`], `default`), for `I` in the interval [0, `last` – `first`).  
  
## Example  
 See the example for [narrow](../vs140/ctype--narrow.md), which calls `do_narrow`.  
  
## Requirements  
 **Header:** <locale\>  
  
 **Namespace:** std  
  
## See Also  
 [ctype Class](../vs140/ctype-Class.md)