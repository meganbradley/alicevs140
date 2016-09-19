---
title: "Compiler Error CS5001"
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
ms.topic: article
ms.assetid: e1e26e75-84e0-47c7-be8a-3c4fd0d6f497
caps.latest.revision: 16
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Compiler Error CS5001
Program 'program' does not contain a static 'Main' method suitable for an entry point  
  
 This error occurs when no static [Main](../Topic/Main\(\)%20and%20Command-Line%20Arguments%20\(C%23%20Programming%20Guide\).md) method with a correct signature is found in the code that produces an executable file. This error also occurs if the entry point function, `Main`, is defined with the wrong case, such as lower-case `main`.  
  
-   `Main` must be declared as static and it must return [void](../vs140/void--C#-Reference-.md) or [int](../Topic/int%20\(C%23%20Reference\).md), and it must have either no parameters or else one parameter of type `string[]`.  
  
## Example  
 The following example generates CS5001:  
  
```  
// CS5001.cs  
// CS5001 expected  
public class a  
{  
   // Uncomment the following line to resolve.  
   // static void Main() {}  
}  
```  
  
## See Also  
 [Main() and Command Line Arguments (C# Programming Guide)](../Topic/Main\(\)%20and%20Command-Line%20Arguments%20\(C%23%20Programming%20Guide\).md)