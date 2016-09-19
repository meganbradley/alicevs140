---
title: "Compiler Error CS0119"
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
ms.assetid: 048924f1-378f-4021-bd20-299d3218f810
caps.latest.revision: 12
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Compiler Error CS0119
'construct1_name' is a 'construct1', which is not valid in the given context.  
  
 The compiler detected an unexpected construct such as the following:  
  
-   A class constructor is not a valid test expression in a conditional statement.  
  
-   A class name was used instead of an instance name to refer to an array element.  
  
-   A method identifier is used as if it were a struct or class  
  
## Example  
 The following sample generates CS0119.  
  
```  
// CS0119.cs  
using System;  
public class MyClass   
{  
   public static void Test() {}  
  
   public static void Main()  
   {  
      Console.WriteLine(Test.x);   // CS0119  
   }  
}  
```