---
title: "Compiler Warning (level 1) C4677"
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
ms.assetid: a8d656a1-e2ff-4f8b-9028-201765131026
caps.latest.revision: 14
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Compiler Warning (level 1) C4677
'function': signature of non-private member contains assembly private type 'private_type'  
  
 A type that has public accessibility outside the assembly uses a type that has private access outside the assembly. A component that references the public assembly type will not be able to use the type member or members that reference the assembly private type.  
  
## Example  
 The following sample generates C4677.  
  
```  
// C4677.cpp  
// compile with: /clr /c /W1  
delegate void TestDel();  
public delegate void TestDel2();  
  
public ref class MyClass {  
public:  
   static event TestDel^ MyClass_Event;   // C4677  
   static event TestDel2^ MyClass_Event2;   // OK  
};  
```