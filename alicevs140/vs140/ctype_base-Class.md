---
title: "ctype_base Class"
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
ms.assetid: ccffe891-d7ab-4d22-baf8-8eb6d438a96d
caps.latest.revision: 19
translation.priority.ht: 
  - de-de
  - ja-jp
---
# ctype_base Class
The class serves as a base class for facets of template class [ctype](../vs140/ctype-Class.md). A base class for the ctype class that is used to define enumeration types used to classify or test characters either individually or within entire ranges.  
  
## Syntax  
  
```  
struct ctype_base : public locale::facet  
{  
    enum  
    {  
        alnum, alpha, cntrl, digit, graph,  
        lower, print, punct, space, upper,  
        xdigit  
    };  
    typedef short mask;  
    ctype_base(  
        size_t _Refs = 0  
    );  
    ~ctype_base();  
};  
```  
  
## Remarks  
 It defines an enumeration mask. Each enumeration constant characterizes a different way to classify characters, as defined by the functions with similar names declared in the header <ctype.h>. The constants are:  
  
-   **space** (function [isspace](../vs140/-locale--functions.md#isspace))  
  
-   **print** (function [isprint](../vs140/-locale--functions.md#isprint))  
  
-   **cntrl** (function [iscntrl](../vs140/-locale--functions.md#iscntrl))  
  
-   **upper** (function [isupper](../vs140/-locale--functions.md#isupper))  
  
-   **lower** (function [islower](../vs140/-locale--functions.md#islower))  
  
-   **digit** (function [isdigit](../vs140/-locale--functions.md#isdigit))  
  
-   **punct** (function [ispunct](../vs140/-locale--functions.md#ispunct))  
  
-   **xdigit** (function [isxdigit](../vs140/-locale--functions.md#isxdigit))  
  
-   **alpha** (function [isalpha](../vs140/-locale--functions.md#isalpha))  
  
-   **alnum** (function [isalnum](../vs140/-locale--functions.md#isalnum))  
  
-   **graph** (function [isgraph](../vs140/-locale--functions.md#isgraph))  
  
 You can characterize a combination of classifications by ORing these constants. In particular, it is always true that **alnum** == ( **alpha**``&#124; **digit**\) and **graph** \=\= \( **alnum**``&#124; **punct**).  
  
## Requirements  
 **Header:** <locale\>  
  
 **Namespace:** std  
  
## See Also  
 [Thread Safety in the Standard C++ Library](../vs140/Thread-Safety-in-the-C---Standard-Library.md)