---
title: "Compiler Error CS0746"
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
ms.assetid: 36baf7f2-b092-422c-ab53-95154bfceb0a
caps.latest.revision: 8
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Compiler Error CS0746
Invalid anonymous type member declarator. Anonymous type members must be declared with a member assignment, simple name or member access.  
  
 An anonymous type must be declared with a member assignment, simple name, or member access.  
  
### To correct this error  
  
1.  Ensure that your declaration uses only member assignment, simple names, or member access expressions.  
  
## Example  
 The following code generates CS0746 in the declaration of `incorrect_1` and `incorrect_2`. The following declarations show two of the correct ways to declare an anonymous type.  
  
```  
// cs0746.cs  
public class C  
{  
    public static int Main()  
    {  
        int i = 100;  
        string s = "Bottles of beer.";  
  
        var incorrect_1 = new { a.b = 1 }; // CS0746   
        var incorrect_2 = new {100, "Bottles of beer."}; // CS0746  
        var correct_1 = new { i, s }; //OK  
        var correct_2 = new {num = i, message = s}; // OK  
  
        return 1;  
    }  
}  
  
```  
  
## See Also  
 [Anonymous Types (C# Programming Guide)](../Topic/Anonymous%20Types%20\(C%23%20Programming%20Guide\).md)