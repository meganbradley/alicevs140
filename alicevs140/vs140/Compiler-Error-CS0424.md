---
title: "Compiler Error CS0424"
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
ms.assetid: 09ae482c-255a-4f99-8dc8-ba31c3ea8c71
caps.latest.revision: 10
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Compiler Error CS0424
'class': a class with the ComImport attribute cannot specify a base class  
  
 Specifying the <xref:System.Runtime.InteropServices.ComImportAttribute?qualifyHint=False> attribute implies that the implementation for the class is to be imported from a COM module. Additional methods or fields inherited from the base class are not allowed to be added to the implementation defined in the COM module.  
  
 The following sample generates CS0424:  
  
```  
// CS0424.cs  
// compile with: /target:library  
using System.Runtime.InteropServices;  
public class A {}  
  
[ ComImport, Guid("7ab770c7-0e23-4d7a-8aa2-19bfad479829") ]  
class B : A {}   // CS0424 error  
```