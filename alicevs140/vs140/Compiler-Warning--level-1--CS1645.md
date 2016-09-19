---
title: "Compiler Warning (level 1) CS1645"
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
ms.assetid: ea45fb20-b696-4d4e-b893-edde9d96bd3a
caps.latest.revision: 9
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Compiler Warning (level 1) CS1645
Feature 'feature' is not part of the standardized ISO C# language specification, and may not be accepted by other compilers  
  
 The feature you are using is not part of the ISO standard. Code using this feature may not compile on other compilers.  
  
```  
// CS1645.cs  
// compile with: /W:1 /t:module /langversion:ISO-1  
[assembly:System.CLSCompliant(false)]  
// To supress the warning use the switch: /nowarn:1645  
[module:System.CLSCompliant(false)]   // CS1645  
class Test  
{  
}  
```