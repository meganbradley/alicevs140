---
title: "Compiler Error CS1716"
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
ms.assetid: c9e65274-0cc3-41a6-967c-ac1804ecf3ba
caps.latest.revision: 13
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Compiler Error CS1716
Do not use 'System.Runtime.CompilerServices.FixedBuffer' attribute. Use the 'fixed' field modifier instead.  
  
 This error arises in an unsafe code section that contains a fixed-size array declaration similar to a field declaration. Do not use this attribute. Instead, use the keyword `fixed`.  
  
## Example  
 The following example generates CS1716.  
  
```  
// CS1716.cs  
// compile with: /unsafe  
using System;  
using System.Runtime.CompilerServices;  
  
public struct UnsafeStruct  
{  
    [FixedBuffer(typeof(int), 4)]  // CS1716  
    unsafe public int aField;  
    // Use this single line instead of the above two lines.  
    // unsafe public fixed int aField[4];  
}  
  
public class TestUnsafe  
{  
    static int Main()  
    {  
        UnsafeStruct us = new UnsafeStruct();  
        unsafe  
        {  
            if (us.aField[0] == 0)  
                return us.aField[1];  
            else  
                return us.aField[2];  
        }  
    }  
}  
```