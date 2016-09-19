---
title: "Compiler Error CS0418"
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
ms.assetid: b78fafde-428b-4fa2-a933-c4614760bb71
caps.latest.revision: 10
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Compiler Error CS0418
'class name': an abstract class cannot be sealed or static  
  
 An abstract class cannot be used to create objects unless it is derived from, so it makes no sense to be sealed. An abstract class cannot meaningfully be static either; abstract classes are designed to support an object hierarchy that will use the abstract class as a base.  
  
## Example  
 The following sample generates CS0418:  
  
```  
// CS0418.cs  
public abstract sealed class C  // CS0418  
{  
}  
  
sealed static class S  // CS0418  
{  
}  
  
public class MyClass  
{  
    public static void Main()  
    {  
    }  
}  
```