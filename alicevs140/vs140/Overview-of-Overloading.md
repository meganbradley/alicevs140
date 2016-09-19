---
title: "Overview of Overloading"
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
ms.assetid: cd012dd4-607c-4f8e-bd2e-2bd506ac81ea
caps.latest.revision: 10
translation.priority.mt: 
  - de-de
  - ja-jp
---
# Overview of Overloading
With the C++ language, you can overload functions and operators. Overloading is the practice of supplying more than one definition for a given function name in the same scope. The compiler is left to pick the appropriate version of the function or operator based on the arguments with which it is called. For example, the function max is considered an overloaded function. It can be used in code such as the following:  
  
```  
// overview_overload.cpp  
double max( double d1, double d2 )  
{  
   return ( d1 > d2 ) ? d1 : d2;  
}  
  
int max( int i1, int i2 )  
{  
   return ( i1 > i2 ) ? i1 : i2;  
}  
int main()  
{  
   int    i = max( 12, 8 );  
   double d = max( 32.9, 17.4 );  
}  
```  
  
 In the first function call, where the maximum value of two variables of type `int` is being requested, the function `max( int, int )` is called. However, in the second function call, the arguments are of type `double`, so the function `max( double, double )` is called.  
  
## See Also  
 [Overloading  (C++)](../vs140/Overloading---C---.md)