---
title: "Compiler Error C3126"
ms.custom: na
ms.date: 09/18/2016
ms.devlang: 
  - C++
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - devlang-cpp
ms.tgt_pltfrm: na
ms.topic: error-reference
ms.assetid: e72658a3-5d85-4a31-89a4-dbc3d475973d
caps.latest.revision: 10
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Compiler Error C3126
cannot define a union 'union' inside of managed type 'type'  
  
 A union cannot be defined inside a managed type.  
  
 The following sample generates C3126:  
  
```  
// C3126_2.cpp  
// compile with: /clr /c  
ref class Test  
{  
   union x  
   {   // C3126  
      int a;  
      int b;  
   };  
};  
```  
  
 The following sample generates C3126:  
  
```  
// C3126.cpp  
// compile with: /clr:oldSyntax /c  
#using <mscorlib.dll>  
  
__gc class Test  
{  
   union x  
   {   // C3126  
      int a;  
      int b;  
   };  
};  
```