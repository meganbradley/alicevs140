---
title: "marshal_context::marshal_as"
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
ms.topic: reference
ms.assetid: 24a1afee-51c0-497c-948c-f77fe43635c8
caps.latest.revision: 16
translation.priority.ht: 
  - de-de
  - ja-jp
---
# marshal_context::marshal_as
Performs the marshaling on a specific data object to convert it between a managed and a native data type.  
  
## Syntax  
  
```  
To_Type marshal_as<To_Type>(  
   From_Type input   
);  
```  
  
#### Parameters  
 [in] `input`  
 The value that you want to marshal to a `To_Type` variable.  
  
## Return Value  
 A variable of type `To_Type` that is the converted value of `input`.  
  
## Remarks  
 This function performs the marshaling on a specific data object. Use this function only with the conversions indicated by the table in [Marshaling Overview in C++](../vs140/Overview-of-Marshaling-in-C--.md).  
  
 If you try to marshal a pair of data types that are not supported, `marshal_as` will generate an error [C4996](../vs140/Compiler-Warning--level-3--C4996.md) at compile time. Read the message supplied with this error for more information. The `C4996` error can be generated for more than just deprecated functions. Two conditions that will generate this error are trying to marshal a pair of data types that are not supported and trying to use `marshal_as` for a conversion that requires a context.  
  
 The marshaling library consists of several header files. Any conversion requires only one file, but you can include additional files if you need to for other conversions. The table in `Marshaling Overview in C++` indicates which marshaling file should be included for each conversion.  
  
## Example  
 This example creates a context for marshaling from a `System::String` to a `const char *` variable type. The converted data will not be valid after the line that deletes the context.  
  
```  
// marshal_context_test.cpp  
// compile with: /clr  
#include <stdlib.h>  
#include <string.h>  
#include <msclr\marshal.h>  
  
using namespace System;  
using namespace msclr::interop;  
  
int main() {  
   marshal_context^ context = gcnew marshal_context();  
   String^ message = gcnew String("Test String to Marshal");  
   const char* result;  
   result = context->marshal_as<const char*>( message );  
   delete context;  
   return 0;  
}  
```  
  
## Requirements  
 **Header file:** <msclr\marshal.h>, <msclr\marshal_windows.h>, <msclr\marshal_cppstd.h>, or <msclr\marshal_atl.h>  
  
 **Namespace:** msclr::interop  
  
## See Also  
 [Marshaling Overview in C++](../vs140/Overview-of-Marshaling-in-C--.md)   
 [marshal_as](../vs140/marshal_as.md)   
 [marshal_context Class](../vs140/marshal_context-Class.md)