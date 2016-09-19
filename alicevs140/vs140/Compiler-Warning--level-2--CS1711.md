---
title: "Compiler Warning (level 2) CS1711"
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
ms.assetid: 0021275a-43eb-4295-929e-bb3283577a11
caps.latest.revision: 14
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Compiler Warning (level 2) CS1711
XML comment on 'type' has a typeparam tag for 'parameter', but there is no type parameter by that name  
  
 The documentation of a generic type includes a tag for the type parameter that has the wrong name.  
  
## Example  
 The following code generates warning CS1711.  
  
```  
// cs1711.cs  
// compile with: /doc:cs1711.xml  
// CS1711 expected  
using System;  
///<typeparam name="WrongName">can be an int</typeparam>  
class CMain  
{  
    public static void Main() { }  
}  
```