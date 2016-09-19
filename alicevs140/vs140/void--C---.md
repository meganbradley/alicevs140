---
title: "void (C++)"
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
ms.topic: language-reference
ms.assetid: d203edba-38e6-4056-8b89-011437351057
caps.latest.revision: 11
translation.priority.ht: 
  - de-de
  - ja-jp
---
# void (C++)
When used as a function return type, the `void` keyword specifies that the function does not return a value. When used for a function's parameter list, void specifies that the function takes no parameters. When used in the declaration of a pointer, void specifies that the pointer is "universal."  
  
 If a pointer's type is **void \***, the pointer can point to any variable that is not declared with the **const** or `volatile` keyword. A void pointer cannot be dereferenced unless it is cast to another type. A void pointer can be converted into any other type of data pointer.  
  
 A void pointer can point to a function, but not to a class member in C++.  
  
 You cannot declare a variable of type void.  
  
## Example  
  
```  
// void.cpp  
void vobject;   // C2182  
void *pv;   // okay  
int *pint; int i;  
int main() {  
   pv = &i;  
   // Cast optional in C required in C++  
   pint = (int *)pv;  
}   
```  
  
## See Also  
 [Keywords](../vs140/Keywords--C---.md)   
 [Pointers to Type void](../vs140/Pointers-to-Type-void.md)   
 [Fundamental Types](../vs140/Fundamental-Types---C---.md)