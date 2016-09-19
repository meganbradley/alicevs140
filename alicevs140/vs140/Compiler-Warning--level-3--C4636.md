---
title: "Compiler Warning (level 3) C4636"
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
ms.assetid: 59112a0f-850f-41c6-bd84-8ae8dc84706a
caps.latest.revision: 12
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Compiler Warning (level 3) C4636
XML document comment applied to 'construct': tag requires non-empty '' attribute.  
  
 A tag, such as `cref`, did not have a value.  
  
## Example  
 The following sample generates C4636.  
  
```  
// C4636.cpp  
// compile with: /clr /doc /W3 /c  
/// <see cref=''/>  
// /// <see cref='System::Exception'/>  
ref struct A {   // C4636  
   void f(int);  
};  
  
// OK  
/// <see cref='System::Exception'/>  
ref struct B {  
   void f(int);  
};  
```