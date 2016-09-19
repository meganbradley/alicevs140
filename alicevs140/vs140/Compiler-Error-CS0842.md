---
title: "Compiler Error CS0842"
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
ms.assetid: 93a8b333-efc4-40c7-ae53-5264f721a74f
caps.latest.revision: 7
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Compiler Error CS0842
Automatically implemented properties cannot be used inside a type marked with StructLayout(LayoutKind.Explicit).  
  
 Auto-implemented properties have their backing fields provided by the compiler and the field is not accessible to source code. Therefore, they are not compatible with <xref:System.Runtime.InteropServices.LayoutKind.Explicit?qualifyHint=True>.  
  
### To correct this error  
  
1.  Make the property a regular property in which you provide the accessor bodies.  
  
## Example  
 The following example generates CS0842:  
  
```  
// cs0842.cs  
using System;  
using System.Runtime.InteropServices;  
  
namespace TestNamespace  
{  
    [StructLayout(LayoutKind.Explicit)]  
    struct Str  
    {  
        public int Num // CS0842  
        {  
            get;  
            set;  
        }  
  
        static int Main()  
        {  
            return 1;  
        }  
    }  
}  
```