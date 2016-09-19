---
title: "operator&lt; &lt;regex&gt;"
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
ms.assetid: 667bed76-46bd-47ea-8857-c6c6898a583e
caps.latest.revision: 20
translation.priority.ht: 
  - de-de
  - ja-jp
---
# operator&lt; &lt;regex&gt;
Less than comparison for various objects.  
  
## Syntax  
  
```  
template<class BidIt>  
    bool operator<(const sub_match<BidIt>& left,  
        const sub_match<BidIt>& right);  
template<class BidIt, class IOtraits, class Alloc>  
    bool operator<(  
        const basic_string<typename iterator_traits<BidIt>::value_type, IOtraits, Alloc>& left,  
        const sub_match<BidIt>& right);  
template<class BidIt, class IOtraits, class Alloc>  
    bool operator<(const sub_match<BidIt>& left,  
        const basic_string<typename iterator_traits<BidIt>::value_type, IOtraits, Alloc>& right);  
template<class BidIt>  
    bool operator<(const typename iterator_traits<BidIt>::value_type *left,  
        const sub_match<BidIt>& right);  
template<class BidIt>  
    bool operator<(const sub_match<BidIt>& left,  
        const typename iterator_traits<BidIt>::value_type *right);  
template<class BidIt>  
    bool operator<(const typename iterator_traits<BidIt>::value_type& left,  
        const sub_match<BidIt>& right);  
template<class BidIt>  
    bool operator<(const sub_match<BidIt>& left,  
        const typename iterator_traits<BidIt>::value_type& right);  
```  
  
#### Parameters  
 `BidIt`  
 The iterator type.  
  
 `IOtraits`  
 The string traits class.  
  
 `Alloc`  
 The allocator class.  
  
 `left`  
 The left object to compare.  
  
 `right`  
 The right object to compare.  
  
## Remarks  
 Each template operator converts its arguments to a string type and returns true only if the converted value of `left` compares less than the converted value of `right`.  
  
## Example  
  
```  
// std_tr1__regex__operator_lt.cpp   
// compile with: /EHsc   
#include <regex>   
#include <iostream>   
  
typedef std::cmatch::string_type Mystr;   
int main()   
    {   
    std::regex rx("c(a*)|(b)");   
    std::cmatch mr;   
  
    std::regex_search("xcaaay", mr, rx);   
  
    std::csub_match sub = mr[1];   
    std::cout << "sub == " << sub << std::endl;   
    std::cout << std::endl;   
  
    std::cout << "sub < sub == " << std::boolalpha   
        << (sub < sub) << std::endl;   
  
    std::cout << "string(\"aab\") < sub == " << std::boolalpha   
        << (Mystr("aab") < sub) << std::endl;   
    std::cout << "sub < string(\"aab\") == " << std::boolalpha   
        << (sub < Mystr("aab")) << std::endl;   
  
    std::cout << "\"aab\" < sub == " << std::boolalpha   
        << ("aab" < sub) << std::endl;   
    std::cout << "sub < \"aab\" == " << std::boolalpha   
        << (sub < "aab") << std::endl;   
  
    std::cout << "'a' < sub == " << std::boolalpha   
        << ('a' < sub) << std::endl;   
    std::cout << "sub < 'a' == " << std::boolalpha   
        << (sub < 'a') << std::endl;   
  
    return (0);   
    }  
  
```  
  
 **sub == aaa**  
**sub < sub == false**  
**string("aab") < sub == false**  
**sub < string("aab") == true**  
**"aab" < sub == false**  
**sub < "aab" == true**  
**'a' < sub == true**  
**sub < 'a' == false**   
## Requirements  
 **Header:** <regex\>  
  
 **Namespace:** std  
  
## See Also  
 [<regex\>](../vs140/-regex-.md)   
 [operator==](../vs140/operator==--regex-.md)   
 [operator!==](../vs140/operator!=--regex-.md)   
 [operator<=](../vs140/operator-=--regex-.md)   
 [operator>](../vs140/operator---regex-.md)   
 [operator>=](../vs140/operator-=--regex-.md)