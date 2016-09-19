---
title: "#pragma warning (C# Reference)"
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
ms.assetid: 723493d5-9753-4cec-babb-54e2b8eb36b6
caps.latest.revision: 19
translation.priority.ht: 
  - de-de
  - ja-jp
---
# #pragma warning (C# Reference)
`#pragma warning` can enable or disable certain warnings.  
  
## Syntax  
  
```  
#pragma warning disable warning-list  
#pragma warning restore warning-list  
```  
  
#### Parameters  
 `warning-list`  
 A comma-separated list of warning numbers. The "CS" prefix is optional.  
  
 When no warning numbers are specified, `disable` disables all warnings and `restore` enables all warnings.  
  
> [!NOTE]
>  To find warning numbers in Visual Studio, build your project and then look for the warning numbers in the **Output** window.  
  
## Example  
  
```  
// pragma_warning.cs  
using System;  
  
#pragma warning disable 414, CS3021  
[CLSCompliant(false)]  
public class C  
{  
    int i = 1;  
    static void Main()  
    {  
    }  
}  
#pragma warning restore CS3021  
[CLSCompliant(false)]  // CS3021  
public class D  
{  
    int i = 1;  
    public static void F()  
    {  
    }  
}  
```  
  
## See Also  
 [C# Reference](../vs140/C#-Reference.md)   
 [C# Programming Guide](../vs140/C#-Programming-Guide.md)   
 [C# Preprocessor Directives](../vs140/C#-Preprocessor-Directives.md)   
 [C# Compiler Errors](../vs140/C#-Compiler-Errors.md)