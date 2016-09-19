---
title: "Using extern to Specify Linkage"
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
ms.assetid: 1e2f0ae3-ae98-4410-85b5-222d6abc865a
caps.latest.revision: 13
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Using extern to Specify Linkage
## Syntax  
  
```  
  
      extern string-literal { declaration-list }  
extern string-literal declaration  
```  
  
## Remarks  
 The `extern` keyword declares a variable or function and specifies that it has external linkage (its name is visible from files other than the one in which it's defined). When modifying a variable, `extern` specifies that the variable has static duration (it is allocated when the program begins and deallocated when the program ends). The variable or function may be defined in another source file, or later in the same file. Declarations of variables and functions at file scope are external by default.  
  
## Example  
  
```  
// specifying_linkage1.cpp  
int i = 1;  
void other();  
  
int main() {  
   // Reference to i, defined above:  
   extern int i;  
}  
  
void other() {  
   // Address of global i assigned to pointer variable:  
   static int *external_i = &i;  
  
   // i will be redefined; global i no longer visible:  
   // int i = 16;  
}  
```  
  
 In C++, when used with a string, `extern` specifies that the linkage conventions of another language are being used for the declarator(s). C functions and data can be accessed only if they are previously declared as having C linkage. However, they must be defined in a separately compiled translation unit.  
  
 Microsoft C++ supports the strings **"C"** and **"C++"** in the *string-literal* field. All of the standard include files use the `extern` "C" syntax to allow the run-time library functions to be used in C++ programs.  
  
## Example  
 The following example shows alternative ways to declare names that have C linkage:  
  
```  
// specifying_linkage2.cpp  
// compile with: /c  
// Declare printf with C linkage.  
extern "C" int printf( const char *fmt, ... );  
  
//  Cause everything in the specified header files  
//   to have C linkage.  
extern "C" {  
   // add your #include statements here  
   #include <stdio.h>  
}  
  
//  Declare the two functions ShowChar and GetChar  
//   with C linkage.  
extern "C" {  
   char ShowChar( char ch );  
   char GetChar( void );  
}  
  
//  Define the two functions ShowChar and GetChar  
//   with C linkage.  
extern "C" char ShowChar( char ch ) {  
   putchar( ch );  
   return ch;  
}  
  
extern "C" char GetChar( void ) {  
   char ch;  
  
   ch = getchar();  
   return ch;  
}  
  
// Declare a global variable, errno, with C linkage.  
extern "C" int errno;  
```  
  
 If a function has more than one linkage specification, they must agree; it is an error to declare functions as having both C and C++ linkage. Furthermore, if two declarations for a function occur in a program — one with a linkage specification and one without — the declaration with the linkage specification must be first. Any redundant declarations of functions that already have linkage specification are given the linkage specified in the first declaration. For example:  
  
```  
extern "C" int CFunc1();  
...  
int CFunc1();            // Redeclaration is benign; C linkage is  
                         //  retained.  
  
int CFunc2();  
...  
extern "C" int CFunc2(); // Error: not the first declaration of  
                         //  CFunc2;  cannot contain linkage  
                         //  specifier.  
```  
  
 Functions and objects explicitly declared as **static** within the body of a compound linkage specifier (**{ }**) are treated as static functions or objects; the linkage specifier is ignored. Other functions and objects behave as if declared using the `extern` keyword. (See [Using extern to Specify Linkage](../vs140/Using-extern-to-Specify-Linkage.md) for details about the `extern` keyword.)  
  
## See Also  
 [Keywords](../vs140/Keywords--C---.md)   
 [(NOTINBUILD)Linkage Specifications](assetId:///d2b0cff1-7798-4c38-9ac8-61c3bfe2bfb9)   
 [extern Storage-Class Specifier](../vs140/extern-Storage-Class-Specifier.md)   
 [Behavior of Identifiers](../vs140/Behavior-of-Identifiers.md)   
 [Linkage](../vs140/Linkage.md)