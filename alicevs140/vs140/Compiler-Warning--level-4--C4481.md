---
title: "Compiler Warning (level 4) C4481"
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
ms.assetid: 7bfd4e0c-b452-4e6c-b7c4-ac5cc93fe4ea
caps.latest.revision: 7
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Compiler Warning (level 4) C4481
nonstandard extension used: override specifier 'keyword'  
  
 A keyword was used that is not in the C++ standard, for example, one of the override specifiers that also works under /clr.  For more information, see,  
  
-   [/clr (Common Language Runtime Compilation)](../Topic/-clr%20\(Common%20Language%20Runtime%20Compilation\).md)  
  
-   [Override Specifiers](../vs140/Override-Specifiers---C---Component-Extensions-.md)  
  
## Example  
 The following sample generates C4481.  
  
```  
// C4481.cpp  
// compile with: /W4 /c  
class B {  
   virtual void f(unsigned);  
};  
  
class C : B {  
   void f(unsigned) override;   // C4481  
   void f2(unsigned);  
};  
```