---
title: "Compiler Warning (level 2) CS0472"
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
ms.topic: article
ms.assetid: dc80e0a3-dbd3-4a81-b8bb-a59b510cd3e1
caps.latest.revision: 6
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Compiler Warning (level 2) CS0472
The result of the expression is always 'value1' since a value of type 'value2' is never equal to 'null' of type 'value3'  
  
 The compiler should warn if you use an operator with a constant null value.  
  
## Example  
 The following sample generates CS0472.  
  
```  
public class Test  
{  
    public static int Main()  
    {  
        int i = 5;  
        int counter = 0;  
  
        // Comparison:  
        if (i == null)  // CS0472  
        // To resolve, use a valid value for i.  
            counter++;   
        return counter;  
    }  
}  
```