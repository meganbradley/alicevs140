---
title: "Compiler Error CS0811"
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
ms.assetid: 99f81ad3-684f-47aa-adb8-360e24901454
caps.latest.revision: 10
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Compiler Error CS0811
The fully qualified name for 'name' is too long for debug information. Compile without '/debug' option.  
  
 There are size constraints on variable and type names in debug information.  
  
### To correct this error  
  
1.  If modifying the name is not possible, the only alternative is to compile without the [/debug](../Topic/-debug%20\(C%23%20Compiler%20Options\).md) option.  
  
## Example  
 The following code generates CS0811:  
  
```  
// cs0811.cs  
//Compile with: /debug  
using System;  
using System.Collections.Generic;  
  
namespace TestNamespace  
{  
    using Long = List<List<List<List<List<List<List<List<List<List<List<List<List  
   <List<List<List<List<List<List<List<List<List<List<List<List<List<List<List<int>>>>>>>>>>>>>>>>>>>>>>>>>>>>; // CS0811  
  
    class Test  
    {  
        static int Main()  
        {  
            return 1;  
        }  
    }  
}  
```