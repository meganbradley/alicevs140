---
title: "Compiler Error CS2019"
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
ms.assetid: eafd2531-8b3a-499c-9e12-a605a011396f
caps.latest.revision: 9
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Compiler Error CS2019
Invalid target type for /target: must specify 'exe', 'winexe', 'library', or 'module'  
  
 The [/target](../Topic/-target%20\(C%23%20Compiler%20Options\).md) compiler option was used, but an invalid parameter was passed. To resolve this error, recompile the program using the form of the **/target** option that is appropriate to your output file.  
  
 The following sample generates CS2017:  
  
```  
// CS2019.cs  
// compile with: /target:libra  
// CS2019 expected  
class MyClass  
{  
}  
```