---
title: "Compiler Error CS0226"
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
ms.assetid: 9f8c74c4-de21-41fb-84e1-ef32a4b23ced
caps.latest.revision: 8
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Compiler Error CS0226
An __arglist expression may only appear inside of a call or new expression.  
  
 The unsupported keyword `__arglist` can only appear in a method call or a new expression.  
  
## Example  
 The following code generates CS0226:  
  
```  
// cs0226.cs  
using System;  
  
public class C  
    {  
    public static int Main ()  
        {  
        __arglist(1,"This is a string"); // CS0226  
        return 0;  
        }  
    }  
```