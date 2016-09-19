---
title: "Compiler Error C3492"
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
ms.assetid: b1dc6342-9133-4b1f-a9c3-e8c65d20d121
caps.latest.revision: 9
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Compiler Error C3492
'var': you cannot capture a member of an anonymous union  
  
 You cannot capture a member of an unnamed union.  
  
### To correct this error  
  
-   Give the union a name and pass the complete union structure to the capture list of the lambda expression.  
  
## Example  
 The following example generates C3492 because it captures a member of an anonymous union:  
  
```  
// C3492a.cpp  
  
int main()  
{  
   union  
   {  
      char ch;  
      int x;  
   };  
  
   ch = 'y';  
   [&x](char ch) { x = ch; }(ch); // C3492  
}  
```  
  
## Example  
 The following example resolves C3492 by giving the union a name and by passing the complete union structure to the capture list of the lambda expression:  
  
```  
// C3492b.cpp  
  
int main()  
{  
   union  
   {  
      char ch;  
      int x;  
   } u;  
  
   u.ch = 'y';  
   [&u](char ch) { u.x = ch; }(u.ch);  
}  
```  
  
## See Also  
 [Lambda Expressions in C++](../vs140/Lambda-Expressions-in-C--.md)