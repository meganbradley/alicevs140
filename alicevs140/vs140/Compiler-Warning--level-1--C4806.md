---
title: "Compiler Warning (level 1) C4806"
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
ms.assetid: 79eb74cd-b925-4b5b-84e1-8ae6f33e38b3
caps.latest.revision: 8
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Compiler Warning (level 1) C4806
'operation' : unsafe operation: no value of type 'type' promoted to type 'type' can equal the given constant  
  
 This message warns against code such as `b == 3`, where `b` has type `bool`. The promotion rules cause `bool` to be promoted to `int`. This is legal, but it can never be **true**. The following sample generates C4806:  
  
```  
// C4806.cpp  
// compile with: /W1  
int main()  
{  
   bool b = true;  
   // try..  
   // int b = true;  
  
   if (b == 3)   // C4806  
   {  
      b = false;  
   }  
}  
```