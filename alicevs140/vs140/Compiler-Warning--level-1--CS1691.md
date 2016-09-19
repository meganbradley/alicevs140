---
title: "Compiler Warning (level 1) CS1691"
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
ms.topic: error-reference
ms.assetid: 7f0fea4d-4215-446c-a249-57daa7e967d2
caps.latest.revision: 10
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Compiler Warning (level 1) CS1691
'number' is not a valid warning number  
  
 A number that was passed to the [#pragma warning](../vs140/#pragma-warning--C#-Reference-.md) preprocessor directive was not a valid warning number. Verify that the number represents a warning, not an error or another sequence of characters.  
  
## Example  
 The following example generates CS1691.  
  
```  
// CS1691.cs  
public class C  
{  
    int i = 1;  
    public static void Main()  
    {  
        C myC = new C();  
#pragma warning disable 151  // CS1691  
// Try the following line instead:  
// #pragma warning disable 1645    
        myC.i++;  
#pragma warning restore 151  // CS1691  
// Try the following line instead:  
// #pragma warning restore 1645    
    }  
}  
```