---
title: "Compiler Error CS0734"
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
ms.assetid: 9e1b0e49-bfc3-400c-9fd1-37e3c827e656
caps.latest.revision: 9
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Compiler Error CS0734
The /moduleassemblyname option may only be specified when building a target type of 'module'  
  
 The compiler option **/moduleassemblyname** should only be used when building a .netmodule. See [/moduleassemblyname (Specify Friend Assembly for Module) (C# Compiler Option)](../vs140/-moduleassemblyname--C#-Compiler-Option-.md) for more information.  
  
 For more information on building a .netmodule, see [/target:module (Create Module to Add to Assembly) (C# Compiler Options)](../vs140/-target-module--C#-Compiler-Options-.md).  
  
## Example  
 The following sample generates CS0734. To resolve, add **/target:module** to the compilation.  
  
```  
// CS0734.cs  
// compile with: /moduleassemblyname:A  
// CS0734 expected  
public class Test {}  
```