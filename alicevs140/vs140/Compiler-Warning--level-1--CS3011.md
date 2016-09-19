---
title: "Compiler Warning (level 1) CS3011"
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
ms.assetid: e27ce521-0147-488b-b4a1-1b6fb5168661
caps.latest.revision: 13
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Compiler Warning (level 1) CS3011
'member': only CLS-compliant members can be abstract  
  
 A class member cannot be both [abstract](../vs140/abstract--C#-Reference-.md) and non-compliant with the Common Language Specification (CLS). The CLS specifies that all class members shall be implemented. For more information about CLS Compliance, see [Writing CLS-Compliant Code](assetId:///4c705105-69a2-4e5e-b24e-0633bc32c7f3) and [What Is the Common Language Specification](assetId:///4f0b77d0-4844-464f-af73-6e06bedeafc6).  
  
## Example  
 The following example generates CS3011:  
  
```  
// CS3011.cs  
  
using System;  
  
[assembly:CLSCompliant(true)]  
public abstract class I  
{  
    [CLSCompliant(false)]  
    public abstract int M();   // CS3011  
  
    // OK  
    [CLSCompliant(false)]  
    public void M2()  
    {  
    }  
}  
  
public class C : I  
{  
    public override int M()  
    {  
        return 1;  
    }  
  
    public static void Main()  
    {  
    }  
}  
```