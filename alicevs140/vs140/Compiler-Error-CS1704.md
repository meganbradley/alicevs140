---
title: "Compiler Error CS1704"
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
ms.topic: error-reference
ms.assetid: da5e89d5-bbb7-47e9-92f6-b03b1602dee4
caps.latest.revision: 14
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Compiler Error CS1704
An assembly with the same simple name 'Assembly Name' has already been imported. Try removing one of the references or sign them to enable side-by-side.  
  
 This error points out that two references have the same assembly identity because the assemblies in question lack strong names, they were not signed, and thus the compiler has no way of distinguishing between them in metadata. Thus, the run time ignores the version and culture assembly name properties. The user should remove the redundant reference, rename one of the references, or provide a strong name for them.  
  
## Example  
 This sample creates an assembly and saves it to the root directory.  
  
```  
// CS1704_a.cs  
// compile with: /target:library /out:c:\\cs1704.dll  
public class A {}  
```  
  
## Example  
 This sample creates an assembly with the same name as the previous sample, but saves it to a different location.  
  
```  
// CS1704_b.cs  
// compile with: /target:library /out:cs1704.dll  
public class A {}  
```  
  
## Example  
 This sample attempts to reference both assemblies. The following sample generates CS1704.  
  
```  
// CS1704_c.cs  
// compile with: /target:library /r:A2=cs1704.dll /r:A1=c:\\cs1704.dll  
// CS1704 expected  
extern alias A1;  
extern alias A2;  
```