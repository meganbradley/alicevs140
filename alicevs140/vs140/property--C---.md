---
title: "property (C++)"
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
ms.assetid: f3b850ba-bf48-4df7-a1d6-8259d97309ce
caps.latest.revision: 9
translation.priority.ht: 
  - de-de
  - ja-jp
---
# property (C++)
**Microsoft Specific**  
  
 This attribute can be applied to non-static "virtual data members" in a class or structure definition. The compiler treats these "virtual data members" as data members by changing their references into function calls.  
  
## Syntax  
  
```  
  
      __declspec( property( get=get_func_name ) ) declarator  
__declspec( property( put=put_func_name ) ) declarator  
__declspec( property( get=get_func_name, put=put_func_name ) ) declarator  
```  
  
## Remarks  
 When the compiler sees a data member declared with this attribute on the right of a member-selection operator ("**.**" or "**->**"), it converts the operation to a **get** or **put** function, depending on whether such an expression is an l-value or an r-value. In more complicated contexts, such as "`+=`", a rewrite is performed by doing both **get** and **put**.  
  
 This attribute can also be used in the declaration of an empty array in a class or structure definition. For example:  
  
```  
__declspec(property(get=GetX, put=PutX)) int x[];  
```  
  
 The above statement indicates that `x[]` can be used with one or more array indices. In this case, `i=p->x[a][b]` will be turned into `i=p->GetX(a, b)`, and `p->x[a][b] = i` will be turned into `p->PutX(a, b, i);`  
  
 **END Microsoft Specific**  
  
## Example  
  
```  
// declspec_property.cpp  
struct S {  
   int i;  
   void putprop(int j) {   
      i = j;  
   }  
  
   int getprop() {  
      return i;  
   }  
  
   __declspec(property(get = getprop, put = putprop)) int the_prop;  
};  
  
int main() {  
   S s;  
   s.the_prop = 5;  
   return s.the_prop;  
}  
```  
  
## See Also  
 [__declspec](../vs140/__declspec.md)   
 [Keywords](../vs140/Keywords--C---.md)