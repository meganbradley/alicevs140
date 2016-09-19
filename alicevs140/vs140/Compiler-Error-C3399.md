---
title: "Compiler Error C3399"
ms.custom: na
ms.date: 09/19/2016
ms.devlang: 
  - C++
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - devlang-csharp
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 306ad199-d150-4f6c-bcf1-24a7948b93be
caps.latest.revision: 5
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Compiler Error C3399
'type' : cannot provide arguments when creating an instance of a generic parameter  
  
 When you specify the `gcnew()` constraint, you specify that the constraint type will have a parameterless constructor. Therefore, it is an error to attempt to instantiate that type and pass a parameter.  
  
 See [Constraints](../vs140/Constraints-on-Generic-Type-Parameters--C---CLI-.md) for more information.  
  
## Example  
 The following sample generates C3399.  
  
```  
// C3399.cpp  
// compile with: /clr /c  
generic <class T>   
where T : gcnew()  
void f() {  
   T t = gcnew T(1);   // C3399  
   T t2 = gcnew T();   // OK  
}  
```