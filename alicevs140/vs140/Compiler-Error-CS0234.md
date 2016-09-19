---
title: "Compiler Error CS0234"
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
ms.assetid: 413774cc-b63e-472b-8fe7-cf23ca970a5f
caps.latest.revision: 14
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Compiler Error CS0234
The type or namespace name 'name' does not exist in the namespace 'namespace' (are you missing an assembly reference?)  
  
 A type was expected. Possible causes for this error include the following:  
  
-   An assembly that contains the definition of a type was not referenced in the compilation; use [/reference (Import Metadata)](../vs140/-reference--C#-Compiler-Options-.md) to specify the assembly  
  
-   You passed a variable name to the [typeof](../Topic/typeof%20\(C%23%20Reference\).md) operator.  
  
-   You tried to reference an assembly that is not part of your target .NET Framework profile. For more information, see [Troubleshooting .NET Framework Targeting Errors](../vs140/Troubleshooting-.NET-Framework-Targeting-Errors.md).  
  
 If you see this error after moving code from one development machine to another, make sure that the project on the new machine has the correct references, and that the versions of the assemblies are the same as on the old machine. You can also use the Object Browser to inspect an assembly and verify whether it contains the types that you expect it to contain.  
  
 The following sample generates CS0234:  
  
```  
// CS0234.cs  
public class C  
{  
   public static void Main()  
   {  
      System.DateTime x = new System.DateTim();   // CS0234  
      // try the following line instead  
      // System.DateTime x = new System.DateTime();  
   }  
}  
```