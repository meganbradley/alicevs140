---
title: "regex_traits::lookup_classname"
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
ms.assetid: d74c20c4-044d-4e93-92a4-19f1f78d9083
caps.latest.revision: 17
translation.priority.ht: 
  - de-de
  - ja-jp
---
# regex_traits::lookup_classname
Maps a sequence to a character class.  
  
## Syntax  
  
```  
template<class FwdIt>  
    char_class_type lookup_classname(FwdIt first, FwdIt last) const;  
```  
  
#### Parameters  
 `first`  
 Beginning of sequence to look up.  
  
 `last`  
 End of sequence to look up.  
  
## Remarks  
 The member function returns a value that designates the character class named by the character sequence pointed to by its arguments. The value does not depend on the case of the characters in the sequence.  
  
 The specialization `regex_traits<char>` recognizes the names `"d"`, `"s"`, `"w"`, `"alnum"`, `"alpha"`, `"blank"`, `"cntrl"`, `"digit"`, `"graph"`, `"lower"`, `"print"`, `"punct"`, `"space"`, `"upper"`, and `"xdigit"`, all without regard to case.  
  
 The specialization `regex_traits<wchar_t>` recognizes the names `L"d"`, `L"s"`, `L"w"`, `L"alnum"`, `L"alpha"`, `L"blank"`, `L"cntrl"`, `L"digit"`, `L"graph"`, `L"lower"`, `L"print"`, `L"punct"`, `L"space"`, `L"upper"`, and `L"xdigit"`, all without regard to case.  
  
## Example  
  
```  
// std_tr1__regex__regex_traits_lookup_classname.cpp   
// compile with: /EHsc   
#include <regex>   
#include <iostream>   
  
typedef std::regex_traits<char> Mytr;   
int main()   
    {   
    Mytr tr;   
  
    Mytr::char_type ch = tr.translate('a');   
    std::cout << "translate('a') == 'a' == " << std::boolalpha   
        << (ch == 'a') << std::endl;   
  
    std::cout << "nocase 'a' == 'A' == " << std::boolalpha   
        << (tr.translate_nocase('a') == tr.translate_nocase('A'))   
        << std::endl;   
  
    const char *lbegin = "abc";   
    const char *lend = lbegin + strlen(lbegin);   
    Mytr::size_type size = tr.length(lbegin);   
    std::cout << "length(\"abc\") == " << size <<std::endl;   
  
    Mytr::string_type str = tr.transform(lbegin, lend);   
    std::cout << "transform(\"abc\") < \"abc\" == " << std::boolalpha   
        << (str < "abc") << std::endl;   
  
    const char *ubegin = "ABC";   
    const char *uend = ubegin + strlen(ubegin);   
    std::cout << "primary \"ABC\" < \"abc\" == " << std::boolalpha   
        << (tr.transform_primary(ubegin, uend) <   
            tr.transform_primary(lbegin, lend))   
        << std::endl;   
  
    const char *dig = "digit";   
    Mytr::char_class_type cl = tr.lookup_classname(dig, dig + 5);   
    std::cout << "class digit == d == " << std::boolalpha   
        << (cl == tr.lookup_classname(dig, dig + 1))   
        << std::endl;   
  
    std::cout << "'3' is digit == " <<std::boolalpha   
        << tr.isctype('3', tr.lookup_classname(dig, dig + 5))   
        << std::endl;   
  
    std::cout << "hex C == " << tr.value('C', 16) << std::endl;   
  
// other members   
    str = tr.lookup_collatename(dig, dig + 5);   
  
    Mytr::locale_type loc = tr.getloc();   
    tr.imbue(loc);   
  
    return (0);   
    }  
  
```  
  
 **translate('a') == 'a' == true**  
**nocase 'a' == 'A' == true**  
**length("abc") == 3**  
**transform("abc") < "abc" == false**  
**primary "ABC" < "abc" == false**  
**class digit == d == true**  
**'3' is digit == true**  
**hex C == 12**   
## Requirements  
 **Header:** <regex\>  
  
 **Namespace:** std  
  
## See Also  
 [<regex\>](../vs140/-regex-.md)   
 [regex_traits](../vs140/regex_traits-Class.md)   
 [regex_traits::lookup_collatename](../vs140/regex_traits--lookup_collatename.md)