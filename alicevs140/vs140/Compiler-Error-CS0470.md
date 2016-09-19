---
title: "Compiler Error CS0470"
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
ms.assetid: b5a8e820-aa5c-4f69-b5c6-01c6a6bb82d9
caps.latest.revision: 8
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Compiler Error CS0470
Method 'method' cannot implement interface accessor 'accessor' for type 'type'. Use an explicit interface implementation.  
  
 This error is generated when an accessor is trying to implement an interface. Explicit interface implementation must be used.  
  
## Example  
 The following sample generates CS0470.  
  
```  
// CS0470.cs  
// compile with: /target:library  
  
interface I  
{  
   int P { get; }  
}  
  
class MyClass : I  
{  
   public int get_P() { return 0; }   // CS0470  
   public int P2 { get { return 0;} }   // OK  
}  
  
```