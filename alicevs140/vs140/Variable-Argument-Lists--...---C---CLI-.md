---
title: "Variable Argument Lists (...) (C++-CLI)"
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
ms.topic: language-reference
H1: Variable Argument Lists (...) (C++/CLI)
ms.assetid: db1a27f4-02a8-4318-8690-1f2893f52b38
caps.latest.revision: 24
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Variable Argument Lists (...) (C++-CLI)
This example shows how you can use the `...` syntax in Visual C++ to implement functions that have a variable number of arguments.  
  
> [!NOTE]
>  This topic pertains to C++/CLI. For information about using the `...` in ISO Standard C++, see [Ellipses and Variadics](../vs140/Ellipses-and-Variadic-Templates.md) and [Ellipses and Default Arguments](../vs140/Ellipses-and-Default-Arguments.md).  
  
 The parameter that uses `...` must be the last parameter in the parameter list.  
  
## Example  
  
### Code  
  
```  
// mcppv2_paramarray.cpp  
// compile with: /clr  
using namespace System;  
double average( ... array<Int32>^ arr ) {  
   int i = arr->GetLength(0);  
   double answer = 0.0;  
  
   for (int j = 0 ; j < i ; j++)  
      answer += arr[j];  
  
   return answer / i;  
}  
  
int main() {  
   Console::WriteLine("{0}", average( 1, 2, 3, 6 ));  
}  
```  
  
### Output  
  
```  
3  
```  
  
## Code Example  
 The following example shows how to call from C# a Visual C++ function that takes a variable number of arguments.  
  
```  
// mcppv2_paramarray2.cpp  
// compile with: /clr:safe /LD  
using namespace System;  
  
public ref class C {  
public:   
   void f( ... array<String^>^ a ) {}  
};  
```  
  
 The function `f` can be called from C# or Visual Basic, for example, as though it were a function that can take a variable number of arguments.  
  
 In C#, an argument that is passed to a `ParamArray` parameter can be called by a variable number of arguments. The following code sample is in C#.  
  
```  
// mcppv2_paramarray3.cs  
// compile with: /r:mcppv2_paramarray2.dll  
// a C# program  
  
public class X {  
   public static void Main() {  
      // Visual C# will generate a String array to match the   
      // ParamArray attribute  
      C myc = new C();  
      myc.f("hello", "there", "world");  
   }  
}  
```  
  
 A call to `f` in Visual C++ can pass an initialized array or a variable-length array.  
  
```  
// mcpp_paramarray4.cpp  
// compile with: /clr  
using namespace System;  
  
public ref class C {  
public:   
   void f( ... array<String^>^ a ) {}  
};  
  
int main() {  
   C ^ myc = gcnew C();  
   myc->f("hello", "world", "!!!");  
}  
```  
  
## See Also  
 [Arrays](../vs140/Arrays--C---Component-Extensions-.md)