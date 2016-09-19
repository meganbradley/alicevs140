---
title: "regex_constants::error_type"
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
ms.assetid: c5cd33f3-dafe-4e48-ad82-a0c3643f92ef
caps.latest.revision: 13
translation.priority.mt: 
  - de-de
  - ja-jp
---
# regex_constants::error_type
Flags for reporting regular expression syntax errors.  
  
## Syntax  
  
```  
typedef T3 error_type;  
static const error_type error_badbrace, error_badrepeat, error_brace,  
  error_brack, error_collate, error_complexity, error_ctype,  
  error_escape, error_paren, error_range, error_space,  
  error_stack, error_backref;  
```  
  
## Remarks  
 The type is an enumerated type that describes an object that can hold error flags. The distinct flag values are:  
  
 `error_badbrace` -- the expression contained an invalid count in a { } expression  
  
 `error_badrepeat` -- a repeat expression (one of '*', '?', '+', '{' in most contexts) was not preceded by an expression  
  
 `error_brace` -- the expression contained an unmatched '{' or '}'  
  
 `error_brack` -- the expression contained an unmatched '[' or ']'  
  
 `error_collate` -- the expression contained an invalid collating element name  
  
 `error_complexity` -- an attempted match failed because it was too complex  
  
 `error_ctype` -- the expression contained an invalid character class name  
  
 `error_escape` -- the expression contained an invalid escape sequence  
  
 `error_paren` -- the expression contained an unmatched '(' or ')'  
  
 `error_range` -- the expression contained an invalid character range specifier  
  
 `error_space` -- parsing a regular expression failed because there were not enough resources available  
  
 `error_stack` -- an attempted match failed because there was not enough memory available  
  
 `error_backref` -- the expression contained an invalid back reference  
  
## Requirements  
 **Header:** <regex\>  
  
 **Namespace:** std  
  
## See Also  
 [<regex\>](../vs140/-regex-.md)   
 [regex_constants](../vs140/regex_constants-Class.md)