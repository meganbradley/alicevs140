---
title: "Compiler Error CS0576"
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
ms.assetid: c409f8ba-4a59-48d3-9bd8-4e9053219875
caps.latest.revision: 15
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Compiler Error CS0576
Namespace 'namespace' contains a definition conflicting with alias 'identifier'  
  
 An attempt was made to use the same namespace twice.  
  
## Example  
 The following sample generates CS0576:  
  
```  
// CS0576.cs  
using SysIO = System.IO;  
public class SysIO  
{  
   public void MyMethod() {}  
}  
  
public class Test  
{  
   public static void Main()  
   {  
      SysIO.Stream s;   // CS0576  
   }  
}  
```