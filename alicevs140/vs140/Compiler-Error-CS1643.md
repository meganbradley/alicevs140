---
title: "Compiler Error CS1643"
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
ms.assetid: 521f352b-00fb-4d62-89be-44251db3cc5b
caps.latest.revision: 10
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Compiler Error CS1643
Not all code paths return a value in method of type 'type!'  
  
 This error occurs if a delegate body does not have a return statement, or has a return statement that the compiler is unable to verify will be reached. In the example below, the compiler does not attempt to predict the result of the branching condition in order to verify that the anonymous method block always returns a value.  
  
## Example  
 The following sample generates CS1643:  
  
```  
// CS1643.cs  
delegate int MyDelegate();  
  
class C  
{  
    static void Main()  
    {  
        MyDelegate d = delegate  
        {                 // CS1643  
            int i = 0;  
            if (i == 0)  
                return 1;  
        };  
    }  
}  
```