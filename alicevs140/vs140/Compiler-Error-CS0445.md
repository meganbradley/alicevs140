---
title: "Compiler Error CS0445"
ms.custom: na
ms.date: 09/18/2016
ms.devlang: 
  - CSharp
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - devlang-csharp
ms.tgt_pltfrm: na
ms.topic: error-reference
ms.assetid: 43f3e5c5-115c-4a34-b0f3-1b7623c49d64
caps.latest.revision: 17
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Compiler Error CS0445
Cannot modify the result of an unboxing conversion  
  
 The result of an unboxing conversion is a temporary variable. The compiler prevents you from modifying such variables because any modification would go away when the temporary variable goes away. To fix this, declare a new value-type variable to store the intermediate expression, and assign the result of the unboxing conversion to that variable.  
  
 The following code generates CS0455.  
  
```c#  
  
// CS0445.CS  
class UnboxingTest  
{  
    public static void Main()  
    {  
        Point p;  
        p.x = 1;  
        p.y = 2;  
        object obj = p;  
        // The following line generates CS0445, because the result  
        // of unboxing obj is a temporary variable.  
        ((Point)obj).x = 2;  
  
        // The following lines resolve the error.  
  
        // Store the result of the unboxing conversion in p2.  
        Point p2;       
        p2 = (Point)obj;  
        // Then you can modify the unboxed value.  
        p2.x = 2;  
    }  
}  
  
struct Point  
{  
    public int x, y;  
}  
  
```