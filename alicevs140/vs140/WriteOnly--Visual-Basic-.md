---
title: "WriteOnly (Visual Basic)"
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
ms.assetid: 488d2899-b09f-4cee-92f0-6f9f9fc4f944
caps.latest.revision: 18
translation.priority.ht: 
  - de-de
  - ja-jp
---
# WriteOnly (Visual Basic)
Specifies that a property can be written but not read.  
  
## Remarks  
  
## Rules  
 **Declaration Context.** You can use `WriteOnly` only at module level. This means the declaration context for a `WriteOnly` property must be a class, structure, or module, and cannot be a source file, namespace, or procedure.  
  
 You can declare a property as `WriteOnly`, but not a variable.  
  
## When to Use WriteOnly  
 Sometimes you want the consuming code to be able to set a value but not discover what it is. For example, sensitive data, such as a social registration number or a password, needs to be protected from access by any component that did not set it. In these cases, you can use a `WriteOnly` property to set the value.  
  
> [!IMPORTANT]
>  When you define and use a `WriteOnly` property, consider the following additional protective measures:  
  
-   **Overriding.** If the property is a member of a class, allow it to default to [NotOverridable](../vs140/NotOverridable--Visual-Basic-.md), and do not declare it `Overridable` or `MustOverride`. This prevents a derived class from making undesired access through an override.  
  
-   **Access Level.** If you hold the property's sensitive data in one or more variables, declare them [Private (Visual Basic)](../vs140/Private--Visual-Basic-.md) so that no other code can access them.  
  
-   **Encryption.** Store all sensitive data in encrypted form rather than in plain text. If malicious code somehow gains access to that area of memory, it is more difficult to make use of the data. Encryption is also useful if it is necessary to serialize the sensitive data.  
  
-   **Resetting.** When the class, structure, or module defining the property is being terminated, reset the sensitive data to default values or to other meaningless values. This gives extra protection when that area of memory is freed for general access.  
  
-   **Persistence.** Do not persist any sensitive data, for example on disk, if you can avoid it. Also, do not write any sensitive data to the Clipboard.  
  
 The `WriteOnly` modifier can be used in this context:  
  
 [Property Statement](../vs140/Property-Statement.md)  
  
## See Also  
 [ReadOnly](../vs140/ReadOnly--Visual-Basic-.md)   
 [Private (Visual Basic)](../vs140/Private--Visual-Basic-.md)   
 [Keywords (Visual Basic)](../vs140/Keywords--Visual-Basic-.md)