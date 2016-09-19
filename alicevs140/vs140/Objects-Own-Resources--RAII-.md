---
title: "Objects Own Resources (RAII)"
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
ms.topic: article
ms.assetid: f86b484e-5a27-4c3b-a92a-dfaa5dd6d93a
caps.latest.revision: 6
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Objects Own Resources (RAII)
Make sure that objects own resources. This principle is also known as “resource acquisition is initialization” or “RAII.”  
  
## Example  
 Pass every “new” object as a constructor argument to another named object that owns it (almost always unique_ptr).  
  
```cpp  
void f() {  
  unique_ptr<widget> p( new widget(…) );  
  my_class x( new widget() );  
  …  
} // automatic destruction and deallocation for both widget objects  
  // automatic exception safety, as if “finally { p->dispose(); x.w.dispose(); }”  
  
```  
  
 Always immediately pass any new resource to another object that owns it.  
  
```cpp  
void g() {  
  other_class y( OpenFile() );  
  …  
} // automatic closing and release for file resource  
  // automatic exception safety, as if “finally { y.file.dispose(); }”  
  
```  
  
## See Also  
 [Welcome Back to C++](../vs140/Welcome-Back-to-C----Modern-C---.md)   
 [C++ Language Reference](../vs140/C---Language-Reference.md)   
 [Standard C++ Library](../vs140/C---Standard-Library-Reference.md)