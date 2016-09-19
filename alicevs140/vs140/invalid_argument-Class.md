---
title: "invalid_argument Class"
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
ms.assetid: af6c227d-ad7c-4e63-9dee-67af81d83506
caps.latest.revision: 19
translation.priority.ht: 
  - de-de
  - ja-jp
---
# invalid_argument Class
The class serves as the base class for all exceptions thrown to report an invalid argument.  
  
## Syntax  
  
```  
class invalid_argument : public logic_error {  
public:  
    explicit invalid_argument(const string& message);  
    explicit invalid_argument(const char *message);  
};  
```  
  
## Remarks  
 The value returned by [what](../vs140/exception-Class.md) is a copy of **message**`.`[data](../vs140/basic_string-Class.md#basic_string__data).  
  
## Example  
  
```  
// invalid_arg.cpp  
// compile with: /EHsc /GR  
#include <bitset>  
#include <iostream>  
  
using namespace std;  
  
int main( )  
{  
   try   
   {  
      bitset< 32 > bitset( string( "11001010101100001b100101010110000") );  
   }  
   catch ( exception &e )   
   {  
      cerr << "Caught " << e.what( ) << endl;  
      cerr << "Type " << typeid( e ).name( ) << endl;  
   };  
}  
\* Output:   
Caught invalid bitset<N> char  
Type class std::invalid_argument  
*\  
```  
  
## Requirements  
 **Header:** <stdexcept\>  
  
 **Namespace:** std  
  
## See Also  
 [logic_error Class](../vs140/logic_error-Class.md)   
 [Thread Safety in the Standard C++ Library](../vs140/Thread-Safety-in-the-C---Standard-Library.md)