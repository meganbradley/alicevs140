---
title: "regex_token_iterator::operator!="
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
ms.assetid: 8c84196f-bb07-4cee-937a-e201eeb0205a
caps.latest.revision: 19
translation.priority.mt: 
  - de-de
  - ja-jp
---
# regex_token_iterator::operator!=
Compares iterators for inequality.  
  
## Syntax  
  
```  
bool operator!=(const regex_token_iterator& right);  
```  
  
#### Parameters  
 `right`  
 The iterator to compare to.  
  
## Remarks  
 The member function returns `!(*this == right)`.  
  
## Example  
  
```  
// std_tr1__regex__regex_token_iterator_operator_ne.cpp   
// compile with: /EHsc   
#include <regex>   
#include <iostream>   
  
typedef std::regex_token_iterator<const char *> Myiter;   
int main()   
    {   
    const char *pat = "aaxaayaaz";   
    Myiter::regex_type rx("(a)a");   
    Myiter next(pat, pat + strlen(pat), rx);   
    Myiter end;   
  
// show whole match   
    for (; next != end; ++next)   
        std::cout << "match == " << next->str() << std::endl;   
    std::cout << std::endl;   
  
// show prefix before match   
    next = Myiter(pat, pat + strlen(pat), rx, -1);   
    for (; next != end; ++next)   
        std::cout << "match == " << next->str() << std::endl;   
    std::cout << std::endl;   
  
// show (a) submatch only   
    next = Myiter(pat, pat + strlen(pat), rx, 1);   
    for (; next != end; ++next)   
        std::cout << "match == " << next->str() << std::endl;   
    std::cout << std::endl;   
  
// show prefixes and submatches   
    std::vector<int> vec;   
    vec.push_back(-1);   
    vec.push_back(1);   
    next = Myiter(pat, pat + strlen(pat), rx, vec);   
    for (; next != end; ++next)   
        std::cout << "match == " << next->str() << std::endl;   
    std::cout << std::endl;   
  
// show prefixes and whole matches   
    int arr[] = {-1, 0};   
    next = Myiter(pat, pat + strlen(pat), rx, arr);   
    for (; next != end; ++next)   
        std::cout << "match == " << next->str() << std::endl;   
    std::cout << std::endl;   
  
// other members   
    Myiter it1(pat, pat + strlen(pat), rx);   
    Myiter it2(it1);   
    next = it1;   
  
    Myiter::iterator_category cat = std::forward_iterator_tag();   
    Myiter::difference_type dif = -3;   
    Myiter::value_type mr = *it1;   
    Myiter::reference ref = mr;   
    Myiter::pointer ptr = &ref;   
  
    dif = dif; // to quiet "unused" warnings   
    ptr = ptr;   
  
    return (0);   
    }  
  
```  
  
 **match == aa**  
**match == aa**  
**match == aa**  
**match ==**   
**match == x**  
**match == y**  
**match == z**  
**match == a**  
**match == a**  
**match == a**  
**match ==**   
**match == a**  
**match == x**  
**match == a**  
**match == y**  
**match == a**  
**match == z**  
**match ==**   
**match == aa**  
**match == x**  
**match == aa**  
**match == y**  
**match == aa**  
**match == z**   
## Requirements  
 **Header:** <regex\>  
  
 **Namespace:** std  
  
## See Also  
 [<regex\>](../vs140/-regex-.md)   
 [regex_token_iterator](../vs140/regex_token_iterator-Class.md)