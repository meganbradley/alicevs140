---
title: "Compiler Warning (level 2) CS0728"
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
ms.assetid: ad6d860d-bac4-48f3-9eab-1efd2b6de6c0
caps.latest.revision: 14
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Compiler Warning (level 2) CS0728
Possibly incorrect assignment to local 'variable' which is the argument to a using or lock statement.  The Dispose call or unlocking will happen on the original value of the local.  
  
 There are several scenarios where `using` or `lock` blocks will result in a temporary leak of resources. Here is one example:  
  
 `thisType f = null;`  
  
 `using (f)`  
  
 `{`  
  
 `f = new thisType();`  
  
 `...`  
  
 `}`  
  
 In this case, the original value, such as null, of the variable `thisType` will be disposed of when the `using` block finishes executing, but the `thisType` object created inside the block will not be, although it will eventually get garbage collected.  
  
 To resolve this error, use the following form:  
  
 `using (thisType f = new thisType())`  
  
 `{`  
  
 `...`  
  
 `}`  
  
 In this case, the newly allocated `thisType` object will be disposed of.  
  
## Example  
 The following code will generate warning CS0728.  
  
```  
// CS0728.cs  
  
using System;  
public class ValidBase : IDisposable  
{  
    public void Dispose() {  }  
}  
  
public class Logger  
{  
    public static void dummy()  
    {  
        ValidBase vb = null;  
        using (vb)   
        {  
            vb = null;  // CS0728  
        }  
        vb = null;  
    }  
    public static void Main() { }  
}  
```