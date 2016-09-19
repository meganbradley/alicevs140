---
title: "abstract  (C++ Component Extensions)"
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
ms.assetid: cbae3408-0378-4ac8-b70d-c016b381a6d5
caps.latest.revision: 23
translation.priority.ht: 
  - de-de
  - ja-jp
---
# abstract  (C++ Component Extensions)
The `abstract` keyword declares either:  
  
-   A type can be used as a base type, but the type itself cannot be instantiated.  
  
-   A type member function can be defined only in a derived type.  
  
## All Platforms  
 **Syntax**  
  
```  
  
      class-declaration  
      class-identifier  
      abstract {}  
virtualreturn-typemember-function-identifier() abstract ;  
  
```  
  
 **Remarks**  
  
 The first example syntax declares a class to be abstract. The *class-declaration* component can be either a native C++ declaration (`class` or `struct`), or a C++ extension declaration (`ref class` or `ref struct`) if the **/ZW** or **/clr** compiler option is specified.  
  
 The second example syntax declares a virtual member function to be abstract. Declaring a function abstract is the same as declaring it a pure virtual function. Declaring a member function abstract also causes the enclosing class to be declared abstract.  
  
 The `abstract` keyword is supported in native and platform-specific code; that is, it can be compiled with or without the **/ZW** or **/clr** compiler option.  
  
 You can detect at compile time if a type is abstract with the `__is_abstract(``type``)` type trait. For more information, see [Intrinsic Support for Type Traits](../vs140/Compiler-Support-for-Type-Traits--C---Component-Extensions-.md).  
  
 The `abstract` keyword is a context-sensitive override specifier. For more information about context-sensitive keywords, see [Context-Sensitive Keywords](../vs140/Context-Sensitive-Keywords---C---Component-Extensions-.md). For more information about override specifiers, see [How to: Declare Override Specifiers in Native Compilations](../vs140/How-to--Declare-Override-Specifiers-in-Native-Compilations--C---CLI-.md).  
  
## [!INCLUDE[wrt](../vs140/includes/wrt_md.md)]  
 For more information, see [Ref classes and structs](http://msdn.microsoft.com/library/windows/apps/hh699870.aspx).  
  
### Requirements  
 Compiler option: **/ZW**  
  
## [!INCLUDE[clr_for_headings](../vs140/includes/clr_for_headings_md.md)]  
  
### Requirements  
 Compiler option: **/clr**  
  
### Examples  
 **Example**  
  
 The following code example generates an error because class `X` is marked `abstract`.  
  
```  
// abstract_keyword.cpp  
// compile with: /clr  
ref class X abstract {  
public:  
   virtual void f() {}  
};  
  
int main() {  
   X ^ MyX = gcnew X;   // C3622  
}  
```  
  
 **Example**  
  
 The following code example generates an error because it instantiates a native class that is marked `abstract`. This error will occur with or without the **/clr** compiler option.  
  
```  
// abstract_keyword_2.cpp  
class X abstract {  
public:  
   virtual void f() {}  
};  
  
int main() {  
   X * MyX = new X; // C3622: 'X': a class declared as 'abstract'  
                    // cannot be instantiated. See declaration of 'X'}  
  
```  
  
 **Example**  
  
 The following code example generates an error because function `f` includes a definition but is marked `abstract`. The final statement in the example shows that declaring an abstract virtual function is equivalent to declaring a pure virtual function.  
  
```  
// abstract_keyword_3.cpp  
// compile with: /clr  
ref class X {  
public:  
   virtual void f() abstract {}   // C3634  
   virtual void g() = 0 {}   // C3634  
};  
```  
  
## See Also  
 [Language Extensions for Runtime Platforms](../Topic/Component%20Extensions%20for%20Runtime%20Platforms.md)