---
title: "Early and Late Binding (Visual Basic)"
ms.custom: na
ms.date: 09/19/2016
ms.devlang: 
  - VB
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - devlang-visual-basic
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: d6ff7f1e-b94f-4205-ab8d-5cfa91758724
caps.latest.revision: 12
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Early and Late Binding (Visual Basic)
The [!INCLUDE[vbprvb](../vs140/includes/vbprvb_md.md)] compiler performs a process called `binding` when an object is assigned to an object variable. An object is *early bound* when it is assigned to a variable declared to be of a specific object type. Early bound objects allow the compiler to allocate memory and perform other optimizations before an application executes. For example, the following code fragment declares a variable to be of type <xref:System.IO.FileStream?qualifyHint=False>:  
  
 [!CODE [VbVbalrOOP#90](../CodeSnippet/VS_Snippets_VBCSharp/VbVbalrOOP#90)]  
  
 Because <xref:System.IO.FileStream?qualifyHint=False> is a specific object type, the instance assigned to `FS` is early bound.  
  
 By contrast, an object is *late bound* when it is assigned to a variable declared to be of type `Object`. Objects of this type can hold references to any object, but lack many of the advantages of early-bound objects. For example, the following code fragment declares an object variable to hold an object returned by the `CreateObject` function:  
  
 [!CODE [VbVbalrOOP#91](../CodeSnippet/VS_Snippets_VBCSharp/VbVbalrOOP#91)]  
  
## Advantages of Early Binding  
 You should use early-bound objects whenever possible, because they allow the compiler to make important optimizations that yield more efficient applications. Early-bound objects are significantly faster than late-bound objects and make your code easier to read and maintain by stating exactly what kind of objects are being used. Another advantage to early binding is that it enables useful features such as automatic code completion and Dynamic Help because the [!INCLUDE[vsprvs](../vs140/includes/vsprvs_md.md)] integrated development environment (IDE) can determine exactly what type of object you are working with as you edit the code. Early binding reduces the number and severity of run-time errors because it allows the compiler to report errors when a program is compiled.  
  
> [!NOTE]
>  Late binding can only be used to access type members that are declared as `Public`. Accessing members declared as `Friend` or `Protected Friend` results in a run-time error.  
  
## See Also  
 <xref:Microsoft.VisualBasic.Interaction.CreateObject?qualifyHint=False>   
 [Object Lifetime: How Objects Are Created and Destroyed](../Topic/Object%20Lifetime:%20How%20Objects%20Are%20Created%20and%20Destroyed%20\(Visual%20Basic\).md)   
 [Object Data Type](../Topic/Object%20Data%20Type.md)