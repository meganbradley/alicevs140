---
title: "Compiler Warning (level 1) CS3008"
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
ms.assetid: 593f6114-bc7b-4789-958f-97bbf99c1c9f
caps.latest.revision: 12
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Compiler Warning (level 1) CS3008
Identifier 'identifier' differing only in case is not CLS-compliant  
  
 A [public](../vs140/public--C#-Reference-.md), [protected](../vs140/protected--C#-Reference-.md), or `protected``internal` identifier breaks compliance with the Common Language Specification (CLS) if it begins with an underscore character (_).For more information on CLS Compliance, see [Writing CLS-Compliant Code](assetId:///4c705105-69a2-4e5e-b24e-0633bc32c7f3) and [What Is the Common Language Specification](assetId:///4f0b77d0-4844-464f-af73-6e06bedeafc6).  
  
## Example  
 The following example generates CS3008:  
  
```  
// CS3008.cs  
  
using System;  
  
[assembly:CLSCompliant(true)]  
public class a  
{  
    public static int _a = 0;  // CS3008  
    // OK, private  
    // private static int _a1 = 0;  
  
    public static void Main()  
    {  
    }  
}  
```