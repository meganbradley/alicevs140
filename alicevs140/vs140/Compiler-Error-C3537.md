---
title: "Compiler Error C3537"
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
ms.assetid: f537ebd1-4fb0-4e09-a453-4f38db2c6881
caps.latest.revision: 8
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Compiler Error C3537
'type': you cannot cast to a type that contains 'auto'  
  
 You cannot cast a variable to the indicated type because the type contains the `auto` keyword and the default [/Zc:auto](../vs140/-Zc-auto--Deduce-Variable-Type-.md) compiler option is in effect.  
  
## Example  
 The following code yields C3537 because the variables are cast to a type that contains the `auto` keyword.  
  
```  
// C3537.cpp  
// Compile with /Zc:auto  
int main()  
{  
   int value = 123;  
   auto(value);                        // C3537  
   (auto)value;                        // C3537  
   auto x1 = auto(value);              // C3537  
   auto x2 = (auto)value;              // C3537  
   auto x3 = static_cast<auto>(value); // C3537  
   return 0;  
}  
```  
  
## See Also  
 [auto Keyword](../vs140/auto-Keyword.md)