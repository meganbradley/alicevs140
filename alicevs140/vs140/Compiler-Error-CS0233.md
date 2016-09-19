---
title: "Compiler Error CS0233"
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
ms.assetid: 75b0123f-2237-43dc-9234-a0f727eee482
caps.latest.revision: 15
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Compiler Error CS0233
'identifier' does not have a predefined size, therefore sizeof can only be used in an unsafe context (consider using System.Runtime.InteropServices.Marshal.SizeOf)  
  
 The [sizeof](../vs140/sizeof--C#-Reference-.md) operator can only be used for types that are compile-time constants. If you are getting this error, make sure that the size of the identifier can be determined at compile time. If it cannot, then use <xref:System.Runtime.InteropServices.Marshal.SizeOf?qualifyHint=False> instead of `sizeof`.  
  
## Example  
 The following example generates CS0233:  
  
```  
// CS0233.cs  
using System;  
using System.Runtime.InteropServices;  
  
[StructLayout(LayoutKind.Sequential)]  
public struct S  
{  
    public int a;  
}  
  
public class MyClass  
{  
    public static void Main()  
    {  
        S myS = new S();  
        Console.WriteLine(sizeof(S));   // CS0233  
        // Try the following line instead:  
        // Console.WriteLine(Marshal.SizeOf(myS));  
   }  
}  
```