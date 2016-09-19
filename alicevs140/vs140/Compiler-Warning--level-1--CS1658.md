---
title: "Compiler Warning (level 1) CS1658"
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
ms.assetid: e67b033d-4c88-4552-b3cd-dfc34546502b
caps.latest.revision: 9
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Compiler Warning (level 1) CS1658
'warning text'. See also error 'error code'  
  
 The compiler emits this warning when it overrides an error with a warning. For information about the problem, refer to the error mentioned. To find the appropriate error from within the Visual Studio IDE, use the index. For example, if the text above reads "See also error 'CS1037'," look for CS1037 in the index.  
  
## Example  
 The following example generates CS1658.  
  
```  
// CS1658.cs  
// compile with: /doc:x.xml  
// CS1584 expected  
/// <summary>  
/// </summary>  
public class C  
{  
    /// <see cref="C.F(params object[])"/>  // CS1658  
    public static void M()  
    {  
    }  
  
    /// <summary>  
    /// </summary>  
    public void F(params object[] o)  
    {  
    }  
  
    static void Main()  
    {  
    }  
}  
```