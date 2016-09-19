---
title: "overflow_error Class"
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
ms.assetid: bae7128d-e36b-4a45-84f1-2f89da441d20
caps.latest.revision: 19
translation.priority.ht: 
  - de-de
  - ja-jp
---
# overflow_error Class
The class serves as the base class for all exceptions thrown to report an arithmetic overflow.  
  
## Syntax  
  
```  
class overflow_error : public runtime_error {  
public:  
    explicit overflow_error(const string& message);  
    explicit overflow_error(const char *message);  
};  
```  
  
## Remarks  
 The value returned by [what](../vs140/exception-Class.md) is a copy of **message**`.`[data](../vs140/basic_string-Class.md#basic_string__data).  
  
## Example  
  
```  
// overflow_error.cpp  
// compile with: /EHsc /GR  
#include <bitset>  
#include <iostream>  
  
using namespace std;  
  
int main( )  
{  
   try   
   {  
      bitset< 33 > bitset;  
      bitset[32] = 1;  
      bitset[0] = 1;  
      unsigned long x = bitset.to_ulong( );  
   }  
   catch ( exception &e )   
   {  
      cerr << "Caught " << e.what( ) << endl;  
      cerr << "Type " << typeid( e ).name( ) << endl;  
   };  
}  
\* Output:   
Caught bitset<N> overflow  
Type class std::overflow_error  
*\  
```  
  
## Requirements  
 **Header:** <stdexcept\>  
  
 **Namespace:** std  
  
## See Also  
 [runtime_error Class](../vs140/runtime_error-Class.md)   
 [Thread Safety in the Standard C++ Library](../vs140/Thread-Safety-in-the-C---Standard-Library.md)