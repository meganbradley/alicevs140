---
title: "-Zc:strictStrings (Disable string literal type conversion)"
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
H1: /Zc:strictStrings (Disable string literal type conversion)
ms.assetid: b7eb3f3b-82c1-48a2-8e63-66bad7397b46
caps.latest.revision: 10
translation.priority.ht: 
  - de-de
  - ja-jp
---
# -Zc:strictStrings (Disable string literal type conversion)
When specified, the compiler requires strict `const`-qualification conformance for pointers initialized by using string literals.  
  
## Syntax  
  
```  
/Zc:strictStrings[-]  
```  
  
## Remarks  
 If **/Zc:strictStrings** is specified, the compiler enforces the standard C++ `const` qualifications for string literals, as type 'array of `const``char`' or 'array of `const``wchar_t`', depending on the declaration. String literals are immutable, and an attempt to modify the contents of one results in an access violation error at run time. You must declare a string pointer as `const` to initialize it by using a string literal, or use an explicit `const_cast` to initialize a non-`const` pointer. By default, or if **/Zc:strictStrings-** is specified, the compiler does not enforce the standard C++ `const` qualifications for string pointers initialized by using string literals.  
  
 Use the **/Zc:strictStrings** option to prevent compilation of incorrect code. This example shows how a simple declaration error leads to a crash at run time:  
  
```cpp  
// strictStrings_off.cpp  
// compile by using: cl /W4 strictStrings_off.cpp  
int main() {  
   wchar_t* str = L"hello";  
   str[2] = L'a'; // run-time error: access violation  
}  
```  
  
 When **/Zc:strictStrings** is enabled, the same code reports an error in the declaration of `str`.  
  
```cpp  
// strictStrings_on.cpp  
// compile by using: cl /Zc:strictStrings /W4 strictStrings_on.cpp  
int main() {  
   wchar_t* str = L"hello"; // error: Conversion from string literal   
   // loses const qualifier  
   str[2] = L'a';   
}  
```  
  
 If you use `auto` to declare a string pointer, the compiler creates the correct `const` pointer type declaration for you. An attempt to modify the contents of a `const` pointer is reported by the compiler as an error.  
  
> [!NOTE]
>  The Standard C++ Library in [!INCLUDE[cpp_dev12_long](../vs140/includes/cpp_dev12_long_md.md)] does not support the **/Zc:strictStrings** compiler option in debug builds. If you see several [C2665](../vs140/Compiler-Error-C2665.md) errors in your build output, this may be the cause.  
  
 For more information about conformance issues in Visual C++, see [Nonstandard Behavior](../vs140/Nonstandard-Behavior.md).  
  
### To set this compiler option in the Visual Studio development environment  
  
1.  Open the project's **Property Pages** dialog box. For details, see [Working with Project Properties](../vs140/Working-with-Project-Properties.md).  
  
2.  Select the **C/C++** folder.  
  
3.  Select the **Command Line** property page.  
  
4.  Modify the **Additional Options** property to include `/Zc:strictStrings` and then choose **OK**.  
  
## See Also  
 [/Zc (Conformance)](../vs140/-Zc--Conformance-.md)