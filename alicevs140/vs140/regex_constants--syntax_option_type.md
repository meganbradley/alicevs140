---
title: "regex_constants::syntax_option_type"
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
ms.assetid: 78e823d0-715e-40cb-b2a5-96ebd4c48492
caps.latest.revision: 13
translation.priority.mt: 
  - de-de
  - ja-jp
---
# regex_constants::syntax_option_type
Flags for selecting syntax options.  
  
## Syntax  
  
```  
typedef T1 syntax_option_type;  
static const syntax_option_type awk, basic, collate, ECMAScript,  
  egrep, extended, grep, icase, nosubs, optimize;  
```  
  
## Remarks  
 The type is a bitmask type that describes language specifiers and syntax modifiers to be used when compiling a regular expression. Options can be combined with `|`. No more than one language specifier should be used at a time.  
  
 The language specifiers are:  
  
 `basic` -- compile as BRE  
  
 `extended` -- compile as ERE  
  
 `ECMAScript` -- compile as ECMAScript  
  
 `awk` -- compile as awk  
  
 `grep` -- compile as grep  
  
 `egrep` -- compile as egrep  
  
 The syntax modifiers are:  
  
 `icase` -- make matches case-insensitive  
  
 `nosubs` -- the implementaton need not keep track of the contents of capture groups  
  
 `optimize` -- the implementation should emphasize speed of matching rather than speed of regular expression compilation  
  
 `collate` -- make matches locale-sensitive  
  
## Requirements  
 **Header:** <regex\>  
  
 **Namespace:** std  
  
## See Also  
 [<regex\>](../vs140/-regex-.md)   
 [regex_constants](../vs140/regex_constants-Class.md)