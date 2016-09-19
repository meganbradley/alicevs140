---
title: "Compiler Error CS0471"
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
ms.assetid: 3b666461-c57b-45f4-83d3-a23786e29ae9
caps.latest.revision: 10
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Compiler Error CS0471
The method 'name' is not a generic method. If you intended an expression list, use parentheses around the < expression.  
  
 This error is generated when your code contains an expression list without parentheses.  
  
## Example  
 The following example generates CS0471.  
  
```  
// CS0471.cs  
// compile with: /t:library  
class Test  
{  
    public void F(bool x, bool y) {}  
    public void F1()  
    {  
        int a = 1, b = 2, c = 3;  
        F(a<b, c>(3));    // CS0471  
        // To resolve, try the following instead:  
        // F((a<b), c>(3));  
    }  
}  
  
```