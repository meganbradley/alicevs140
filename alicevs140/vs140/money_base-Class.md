---
title: "money_base Class"
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
ms.assetid: 1a303c15-9272-4f26-ae16-dcf43a0fd38a
caps.latest.revision: 19
translation.priority.ht: 
  - de-de
  - ja-jp
---
# money_base Class
The class describes an enumeration and a structure common to all specializations of template class [moneypunct](../vs140/moneypunct-Class.md).  
  
## Syntax  
  
```  
struct money_base : public locale::facet  
{  
    enum  
    {  
        symbol = '$',  
        sign = '+',  
        space = ' ',  
        value = 'v',  
        none = 'x'  
    };  
    typedef int part;  
    struct pattern  
    {  
        char field[_PATTERN_FIELD_SIZE];  
    };  
    money_base(  
        size_t _Refs = 0  
    );  
    ~money_base();  
};  
```  
  
## Remarks  
 The enumeration **part** describes the possible values in elements of the array field in the structure pattern. The values of **part** are:  
  
-   **none** to match zero or more spaces or generate nothing.  
  
-   **sign** to match or generate a positive or negative sign.  
  
-   **space** to match zero or more spaces or generate a space.  
  
-   **symbol** to match or generate a currency symbol.  
  
-   **value** to match or generate a monetary value.  
  
## Requirements  
 **Header:** <locale\>  
  
 **Namespace:** std  
  
## See Also  
 [Thread Safety in the Standard C++ Library](../vs140/Thread-Safety-in-the-C---Standard-Library.md)