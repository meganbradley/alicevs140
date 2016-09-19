---
title: "Compiler Warning (level 1) CS3023"
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
ms.assetid: fd7782f9-f18a-4ce8-843b-95bf19b54317
caps.latest.revision: 10
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Compiler Warning (level 1) CS3023
CLSCompliant attribute has no meaning when applied to return types.  Try putting it on the method instead.  
  
 Function return types are not checked for CLS Compliance, since the CLS Compliance rules apply to methods and type declarations.  
  
## Example  
 The following example generates warning CS3023:  
  
```  
// C3023.cs  
  
[assembly:System.CLSCompliant(true)]  
public class Test  
{  
    [return:System.CLSCompliant(true)]  // CS3023  
    // Try this instead:  
    // [method:System.CLSCompliant(true)]  
    public static int Main()  
    {  
        return 0;  
    }  
}  
```