---
title: "ios_base::failure"
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
ms.assetid: f8578c47-c17e-4dae-80dd-1e710fe26e7f
caps.latest.revision: 21
translation.priority.ht: 
  - de-de
  - ja-jp
---
# ios_base::failure
The class `failure` defines the base class for the types of all objects thrown as exceptions, by functions in the `iostreams` library, to report errors detected during stream buffer operations.  
  
## Syntax  
  
```  
namespace std {  
    class failure : public system_error {  
    public:  
        explicit failure(  
            const string& _Message,   
            const error_code& _Code = io_errc::stream  
        );  
        explicit failure(  
            const char* _Str,   
            const error_code& _Code = io_errc::stream  
        );  
};  
```  
  
## Remarks  
 The value returned by `what``()` is a copy of `_Message`, possibly augmented with a test based on `_Code`. If `_Code` is not specified, the default value is `make_error_code``(io_errc::stream)`.  
  
## Example  
  
```  
// ios_base_failure.cpp  
// compile with: /EHsc  
#include <iostream>  
#include <fstream>  
  
int main ( )   
{  
   using namespace std;  
   fstream file;  
   file.exceptions(ios::failbit);  
   try   
   {  
      file.open( "rm.txt", ios_base::in );  
      // Opens nonexistent file for reading  
   }  
   catch( ios_base::failure f )   
   {  
      cout << "Caught an exception: " << f.what() << endl;  
   }  
}  
```  
  
 **Caught an exception: ios_base::failbit set**   
## Requirements  
 **Header:** <ios\>  
  
 **Namespace:** std  
  
## See Also  
 [ios_base Class](../vs140/ios_base-Class.md)   
 [system_error](../vs140/system_error-Class.md)   
 [iostream Programming](../vs140/iostream-Programming.md)   
 [iostreams Conventions](../vs140/iostreams-Conventions.md)