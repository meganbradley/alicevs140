---
title: "Compiler Warning (level 3) C4800"
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
ms.assetid: 4f409799-a250-45ed-bb5f-657691b0d9f7
caps.latest.revision: 8
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Compiler Warning (level 3) C4800
'type' : forcing value to bool 'true' or 'false' (performance warning)  
  
 This warning is generated when a value that is not `bool` is assigned or coerced into type `bool`. Typically, this message is caused by assigning `int` variables to `bool` variables where the `int` variable contains only values **true** and **false**, and could be redeclared as type `bool`. If you cannot rewrite the expression to use type `bool`, then you can add "`!=0`" to the expression, which gives the expression type `bool`. Casting the expression to type `bool` will not disable the warning, which is by design.  
  
 The following sample generates C4800:  
  
```  
// C4800.cpp  
// compile with: /W3  
int main() {  
   int i = 0;  
  
   // try..  
   // bool i = 0;  
  
   bool j = i;   // C4800  
   j++;  
}  
```