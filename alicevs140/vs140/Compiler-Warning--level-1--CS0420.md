---
title: "Compiler Warning (level 1) CS0420"
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
ms.assetid: 0f52f508-286e-493d-9151-180e05397bf9
caps.latest.revision: 9
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Compiler Warning (level 1) CS0420
'identifier': a reference to a volatile field will not be treated as volatile  
  
 A volatile field should not normally be passed using a `ref` or **out** parameter, since it will not be treated as volatile within the scope of the function. There are exceptions to this, such as when calling an interlocked API. As with any warning, you may use the [#pragma warning](../vs140/#pragma-warning--C#-Reference-.md) to disable this warning in those rare cases where you are intentionally using a volatile field as a reference parameter.  
  
 The following sample generates CS0420:  
  
```  
// CS0420.cs  
// compile with: /W:1  
using System;  
  
class TestClass  
{  
   private volatile int i;  
  
   public void TestVolatile(ref int ii)  
   {  
   }  
  
   public static void Main()  
   {  
      TestClass x = new TestClass();  
      x.TestVolatile(ref x.i);   // CS0420   
   }  
}  
```