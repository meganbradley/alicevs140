---
title: "-Zc:inline (Remove unreferenced COMDAT)"
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
H1: /Zc:inline (Remove unreferenced COMDAT)
ms.assetid: a4c94224-1d73-4bea-a9d5-4fa73dc924df
caps.latest.revision: 9
translation.priority.ht: 
  - de-de
  - ja-jp
---
# -Zc:inline (Remove unreferenced COMDAT)
Removes unreferenced functions or data that are COMDATs or only have internal linkage. When **/Zc:inline** is specified, the compiler requires that translation units that use inline data or inline functions must also include the definitions for the data or functions.  
  
## Syntax  
  
```  
/Zc:inline[-]  
```  
  
## Remarks  
 When **/Zc:inline** is specified, the compiler does not emit symbol information for unreferenced COMDAT functions or data, or for functions or data that have internal linkage only. By default, this option is off (**/Zc:inline-**). This optimization simplifies some of the work performed by the linker in release builds or when the linker option [/OPT:REF](../Topic/-OPT%20\(Optimizations\).md) is specified. When the compiler performs this optimization, it can significantly reduce .obj file size and improve linker speeds. This compiler option is not enabled when optimizations are disabled ([/Od](../Topic/-Od%20\(Disable%20\(Debug\)\).md)) or when [/GL (Whole Program Optimization)](../Topic/-GL%20\(Whole%20Program%20Optimization\).md) is specified.  
  
 If **/Zc:inline** is specified, the compiler enforces the C++11 requirement that all functions declared `inline` must have a definition available in the same translation unit if they are used. When the option is not specified, [!INCLUDE[vcprvc](../vs140/includes/vcprvc_md.md)] allows non-conformant code that invokes functions declared `inline` even if no definition is visible. For more information, see the C++11 standard, in section 3.2 and section 7.1.2. This compiler option was introduced in Visual Studio 2013 Update 2.  
  
 To use the **/Zc:inline** option, update non-compliant code. This example shows how the non-compliant use of an inline function declaration without a definition still compiles and links when the default **/Zc:inline-** option is used:  
  
```cpp  
// example.h  
// Compile by using: cl /W4 /EHsc /O2 zcinline.cpp example.cpp  
#pragma once  
  
class Example {  
public:  
   inline void inline_call(); // declared but not defined inline  
   void normal_call();  
   Example() {};  
};  
```  
  
```cpp  
// example.cpp  
// Compile by using: cl /W4 /EHsc /O2 zcinline.cpp example.cpp  
#include <stdio.h>  
#include "example.h"  
  
void Example::inline_call() {  
   printf("inline_call was called.\n");   
}  
  
void Example::normal_call() {  
   printf("normal_call was called.\n");   
   inline_call(); // with /Zc:inline-, inline_call forced into .obj file  
}  
```  
  
```cpp  
// zcinline.cpp  
// Compile by using: cl /W4 /EHsc /O2 zcinline.cpp example.cpp  
#include "example.h"  
  
void main() {  
   Example example;  
   example.inline_call(); // normal call when definition unavailable  
}  
```  
  
 When **/Zc:inline** is enabled, the same code causes a [LNK2019](../vs140/Linker-Tools-Error-LNK2019.md) error, because the compiler does not emit a non-inlined code body for `Example::inline_call` in example.obj. This causes the non-inlined call in `main` to reference an undefined external symbol.  
  
 To resolve this error, you can remove the `inline` keyword from the declaration of `Example::inline_call`, move the definition of `Example::inline_call` into the header file, or move the implementation of `Example` into main.cpp. The next example moves the definition into the header file, where it is visible to any caller that includes the header.  
  
```cpp  
// example2.h  
// Compile by using: cl /W4 /EHsc /O2 zcinline2.cpp example2.cpp  
#pragma once  
#include <stdio.h>  
  
class Example2 {  
public:  
   inline void inline_call() {  
      printf("inline_call was called.\n");   
   }  
   void normal_call();  
   Example2() {};  
};  
```  
  
```cpp  
// example2.cpp  
// Compile by using: cl /W4 /EHsc /O2 zcinline2.cpp example2.cpp  
#include "example2.h"  
  
void Example2::normal_call() {  
   printf("normal_call was called.\n");   
   inline_call();   
}  
```  
  
```cpp  
// zcinline2.cpp  
// Compile by using: cl /W4 /EHsc /O2 zcinline2.cpp example2.cpp  
#include "example2.h"  
  
void main() {  
   Example2 example2;  
   example2.inline_call(); // normal call when definition unavailable  
}  
```  
  
 For more information about conformance issues in Visual C++, see [Nonstandard Behavior](../vs140/Nonstandard-Behavior.md).  
  
### To set this compiler option in the Visual Studio development environment  
  
1.  Open the project's **Property Pages** dialog box. For details, see [Working with Project Properties](../vs140/Working-with-Project-Properties.md).  
  
2.  Select the **C/C++** folder.  
  
3.  Select the **Command Line** property page.  
  
4.  Modify the **Additional Options** property to include `/Zc:inline` and then choose **OK**.  
  
## See Also  
 [/Zc (Conformance)](../vs140/-Zc--Conformance-.md)