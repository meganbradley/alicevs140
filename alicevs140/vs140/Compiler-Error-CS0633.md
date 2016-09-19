---
title: "Compiler Error CS0633"
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
ms.assetid: a24d310b-151a-45eb-b150-3407940ec24c
caps.latest.revision: 16
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Compiler Error CS0633
The argument to the 'attribute' attribute must be a valid identifier  
  
 Any argument that you pass to the <xref:System.Diagnostics.ConditionalAttribute?qualifyHint=False> or <xref:System.Runtime.CompilerServices.IndexerNameAttribute?qualifyHint=False> attributes must be a valid identifier. This means that it may not contain characters such as "+" that are illegal when they occur in identifiers.  
  
## Example  
 This example illustrates CS0633 using the <xref:System.Diagnostics.ConditionalAttribute?qualifyHint=False>. The following sample generates CS0633.  
  
```  
// CS0633a.cs  
#define DEBUG  
using System.Diagnostics;  
public class Test  
{  
   [Conditional("DEB+UG")]   // CS0633  
   // try the following line instead  
   // [Conditional("DEBUG")]  
   public static void Main() { }  
}  
```  
  
## Example  
 This example illustrates CS0633 using the <xref:System.Runtime.CompilerServices.IndexerNameAttribute?qualifyHint=False>.  
  
```  
// CS0633b.cs  
// compile with: /target:module  
#define DEBUG  
using System.Runtime.CompilerServices;  
public class Test  
{  
   [IndexerName("Invalid+Identifier")]   // CS0633  
   // try the following line instead  
   // [IndexerName("DEBUG")]  
   public int this[int i]   
   {   
      get { return i; }   
   }  
}  
  
```