---
title: "runtime_error Class"
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
ms.assetid: 4d0227bf-847b-45a2-a320-2351ebf98368
caps.latest.revision: 19
translation.priority.mt: 
  - de-de
  - ja-jp
---
# runtime_error Class
The class serves as the base class for all exceptions thrown to report errors presumably detectable only when the program executes.  
  
## Syntax  
  
```  
class runtime_error : public exception {  
public:  
    explicit runtime_error(const string& message);  
    explicit runtime_error(const char *message);  
};  
```  
  
## Remarks  
 The value returned by [what](../vs140/exception-Class.md) is a copy of **message**`.`[data](../vs140/basic_string-Class.md#basic_string__data).  
  
## Example  
  
```  
// runtime_error.cpp  
// compile with: /EHsc /GR  
#include <iostream>  
  
using namespace std;  
  
int main( )  
{  
// runtime_error  
   try   
   {  
      locale loc( "test" );  
   }  
   catch ( exception &e )   
   {  
      cerr << "Caught " << e.what( ) << endl;  
      cerr << "Type " << typeid( e ).name( ) << endl;  
   };  
}  
\* Output:   
Caught bad locale name  
Type class std::runtime_error  
*\  
```  
  
## Requirements  
 **Header:** <stdexcept\>  
  
 **Namespace:** std  
  
## See Also  
 [exception Class](../vs140/exception-Class.md)   
 [Thread Safety in the Standard C++ Library](../vs140/Thread-Safety-in-the-C---Standard-Library.md)