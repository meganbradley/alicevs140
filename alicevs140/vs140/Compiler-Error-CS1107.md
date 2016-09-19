---
title: "Compiler Error CS1107"
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
ms.assetid: 1b6f6790-53af-4261-a14f-bf2db9790f0b
caps.latest.revision: 10
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Compiler Error CS1107
A parameter can only have one 'modifier name' modifier.  
  
 It is an error for parameter modifiers such as `this`, `ref`, and `out` to appear more than one time in a parameter definition.  
  
## Example  
 The following example generates CS1107:  
  
```  
// cs1107.cs  
public static class Test  
{  
    // Extension methods.  
        public static void TestMethod(this this t) {} // CS1107  
  
    // Regular Instance Method  
        public void TestMethod(ref ref int i) {} // CS1107  
  
}  
```