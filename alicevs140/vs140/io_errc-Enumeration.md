---
title: "io_errc Enumeration"
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
ms.assetid: ae77a256-df53-446d-8765-6fccf41c4eb6
caps.latest.revision: 9
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# io_errc Enumeration
Provides symbolic names for the error conditions in <iostream\>. Can be used to create [error_condition](../vs140/error_condition-Class.md) objects to be compared with the value that's returned by the [ios_base::failure](../vs140/ios_base--failure.md)`code()` function.  
  
## Syntax  
  
```  
enum class io_errc {  
    stream = 1  
};  
```  
  
## Remarks  
 Both [std::make_error_code()](../vs140/make_error_code.md) and [std::make_error_condition()](../vs140/make_error_condition.md) are overloaded for this enum.  
  
 `ios_base::failure` can contain categories of error codes other than `error_condition`.  
  
## Example  
  
```cpp  
  
// io_errc.cpp  
// cl.exe /nologo /W4 /EHsc /MTd  
  
#include <iostream>       
  
using namespace std;  
  
int main()  
{  
    cin.exceptions(ios::failbit | ios::badbit);  
  
    try {  
        cin.rdbuf(nullptr); // throws io_errc::stream  
    }  
    catch (ios::failure& e) {  
        cerr << "ios failure caught: ";  
        if (e.code() == make_error_condition(io_errc::stream)) {  
            cerr << "io_errc stream error condition" << endl;  
        }  
        else {  
            cerr << "unmatched error condition code " << e.code() << endl;  
        }  
    }  
}  
```  
  
## Output  
  
```  
ios failure caught: io_errc stream error condition  
```  
  
## Requirements  
 **Header:** <system_error>  
  
 **Namespace:** std  
  
## See Also  
 [<system_error>](../vs140/-system_error-.md)