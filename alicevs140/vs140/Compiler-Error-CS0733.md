---
title: "Compiler Error CS0733"
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
ms.assetid: 1b0150e0-48d3-4b9c-85cc-27346e4f5f84
caps.latest.revision: 9
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Compiler Error CS0733
Cannot forward generic type, 'GenericType<>'  
  
## Example  
 The following example generates CS0733. Compile the first file as a library, and then reference it when you compile the second file.  
  
```  
// CS0733a.cs  
// compile with: /target:library  
public class GenericType<T>   
{  
}  
```  
  
```  
// CS0733.cs  
// compile with: /target:library /r:CS0733a.dll  
[assembly: System.Runtime.CompilerServices.TypeForwardedTo(typeof(GenericType<int>))]   // CS0733  
```