---
title: "Compiler Error C2261"
ms.custom: na
ms.date: 09/19/2016
ms.devlang: 
  - C++
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - devlang-cpp
ms.tgt_pltfrm: na
ms.topic: error-reference
ms.assetid: 60969482-9e83-49b5-9631-a04bc844da12
caps.latest.revision: 11
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Compiler Error C2261
'string' : assembly reference is invalid and cannot be resolved  
  
 A value was not valid.  
  
 <xref:System.Runtime.CompilerServices.InternalsVisibleToAttribute?qualifyHint=False> is used to specify a friend assembly. For example, if a.dll wants to specify b.dll as a friend assembly, you would specify (in a.dll): InternalsVisibleTo("b"). The runtime then allows b.dll to access everything in a.dll (except private types).  
  
 For more on the correct syntax when specifying friend assemblies, see [Friend Assemblies](../Topic/Friend%20Assemblies%20\(C++\).md).  
  
## Example  
 The following sample generates C2261.  
  
```  
// C2261.cpp  
// compile with: /clr /c  
using namespace System::Runtime::CompilerServices;  
[assembly: InternalsVisibleTo("a,a,a")];   // C2261  
[assembly: InternalsVisibleTo("a.a")];   // OK  
[assembly: InternalsVisibleTo("a")];   // OK  
```