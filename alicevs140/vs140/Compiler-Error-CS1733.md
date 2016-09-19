---
title: "Compiler Error CS1733"
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
ms.assetid: 2188aabe-404d-4a95-a11a-736dbd848508
caps.latest.revision: 10
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Compiler Error CS1733
Expected expression.  
  
 This error is produced whenever the compiler is expecting an expression on the line where the error occurred. In the following example, the trailing comma in the initializer indicates to the compiler that another expression will follow.  
  
### To correct this error  
  
-   Provide the missing expression.  
  
-   Remove the tokens that are causing the compiler to expect an expression.  
  
## Example  
 The following example produces CS1733 because of the trailing comma:  
  
```  
// cs1733.cs  
using System.Collections.Generic;  
public class Test  
{  
    public static void Main()  
    {  
        List<int> list = new List<int>() {{ 1, 2, }};// CS1733  
    }      
}  
```