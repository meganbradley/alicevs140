---
title: "Compiler Error C3354"
ms.custom: na
ms.date: 09/18/2016
ms.devlang: 
  - C++
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - devlang-csharp
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 185de401-231e-4999-a149-172ee4c69d84
caps.latest.revision: 12
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Compiler Error C3354
'function' : the function used to create a delegate cannot have return type 'type'  
  
 The following types are invalid as return types for a [delegate](../vs140/__delegate.md):  
  
-   Pointer to function  
  
-   Pointer to member  
  
-   Pointer to member function  
  
-   Reference to function  
  
-   Reference to member function  
  
 The following sample generates C3354:  
  
```  
// C3354_2.cpp  
// compile with: /clr /c  
using namespace System;  
typedef void ( *VoidPfn )();  
  
delegate VoidPfn func(); // C3354  
// try the following line instead  
// delegate  void func();  
```  
  
 The following sample generates C3354:  
  
```  
// C3354.cpp  
// compile with: /clr:oldSyntax /c  
#using <mscorlib.dll>  
using namespace System;  
  
typedef void (*VoidPfn)();  
  
__delegate VoidPfn func();   // C3354  
// try the following line instead  
// __delegate void func();  
```