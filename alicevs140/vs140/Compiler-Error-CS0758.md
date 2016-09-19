---
title: "Compiler Error CS0758"
ms.custom: na
ms.date: 09/19/2016
ms.devlang: 
  - CSharp
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - devlang-csharp
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 06ddd548-1311-40db-9078-8a18107b8346
caps.latest.revision: 7
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Compiler Error CS0758
Both partial method declarations must use a params parameter or neither may use a params parameter  
  
 If one part of a partial method specifies a `params` parameter, the other part must specify one also.  
  
### To correct this error  
  
1.  Either add the `params` modifier in one part of the method, or remove it in the other.  
  
## Example  
 The following code generates CS0758:  
  
```  
using System;  
  
    public partial class C  
    {  
        partial void Part(int i, params char[] array);  
        partial void Part(int i, char[] array) // CS0758  
        {  
        }  
  
        public static int Main()  
        {  
            return 1;  
        }  
  
    }  
```  
  
## See Also  
 [Partial Classes and Methods (C# Programming Guide)](../vs140/Partial-Classes-and-Methods--C#-Programming-Guide-.md)   
 [params (C# Reference)](../vs140/params--C#-Reference-.md)