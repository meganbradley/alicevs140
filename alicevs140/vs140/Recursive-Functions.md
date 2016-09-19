---
title: "Recursive Functions"
ms.custom: na
ms.date: 09/19/2016
ms.devlang: 
  - C++
  - C
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - devlang-cpp
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 59739040-3081-4006-abbc-9d8423992bce
caps.latest.revision: 9
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Recursive Functions
Any function in a C program can be called recursively; that is, it can call itself. The number of recursive calls is limited to the size of the stack. See the [/STACK (Stack Allocations)](../vs140/-STACK--Stack-Allocations-.md) (/STACK) linker option for information about linker options that set stack size. Each time the function is called, new storage is allocated for the parameters and for the **auto** and **register** variables so that their values in previous, unfinished calls are not overwritten. Parameters are only directly accessible to the instance of the function in which they are created. Previous parameters are not directly accessible to ensuing instances of the function.  
  
 Note that variables declared with **static** storage do not require new storage with each recursive call. Their storage exists for the lifetime of the program. Each reference to such a variable accesses the same storage area.  
  
## Example  
 This example illustrates recursive calls:  
  
```  
int factorial( int num );      /* Function prototype */  
  
int main()  
{  
    int result, number;  
    .  
    .  
    .  
    result = factorial( number );  
}  
  
int factorial( int num )      /* Function definition */  
{  
    .  
    .  
    .  
    if ( ( num > 0 ) || ( num <= 10 ) )  
        return( num * factorial( num - 1 ) );  
}  
  
```  
  
## See Also  
 [Function Calls](../vs140/Function-Calls.md)