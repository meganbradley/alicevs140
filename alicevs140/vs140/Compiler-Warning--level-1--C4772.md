---
title: "Compiler Warning (level 1) C4772"
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
ms.topic: error-reference
ms.assetid: dafe6fd8-9faf-41f5-9d66-a55838742c14
caps.latest.revision: 12
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Compiler Warning (level 1) C4772
\#import referenced a type from a missing type library; 'missing_type' used as a placeholder  
  
 A type library was referenced with the [#import](../vs140/#import-Directive--C---.md) directive. However, the type library contained a reference to another type library that was not referenced with `#import`. This other .tlb file was not found by the compiler.  
  
 Note that the compiler will not find type libraries in different directories if you use the [/I (Additional Include Directories)](../vs140/-I--Additional-Include-Directories-.md) compiler option to specify those directories. If you want the compiler to find type libraries in different directories, add those directories to the PATH environment variable.  
  
 This warning is, by default, issued as an error. C4772 can not be suppressed with /W0.  
  
## Example  
 This is the first type library needed to reproduce C4772.  
  
```  
// c4772a.idl  
[uuid("f87070ba-c6d9-405c-a8e4-8cd9ca25c12b")]  
library C4772aLib  
{  
   [uuid("f87070ba-c6d9-405c-a8e4-8cd9ca25c100")]  
   enum E_C4772a  
   {  
      one, two, three  
   };  
};  
```  
  
## Example  
 This is the second type library needed to reproduce C4772.  
  
```  
// c4772b.idl  
// post-build command: del /f C4772a.tlb  
// C4772a.tlb is available when c4772b.tlb is built  
[uuid("f87070ba-c6d9-405c-a8e4-8cd9ca25c12d")]  
library C4772bLib  
{  
   importlib ("c4772a.tlb");  
   [uuid("f87070ba-c6d9-405c-a8e4-8cd9ca25c12e")]  
   struct S_C4772b  
   {  
      enum E_C4772a e;  
   };  
};  
```  
  
## Example  
 The following sample generates C4772:  
  
```  
// C4772.cpp  
// assumes that C4772a.tlb is not available to the compiler  
// #import "C4772a.tlb"  
#import "C4772b.tlb"   // C4772 uncomment previous line to resolve  
                       // and make sure c4772a.tlb is on disk  
```