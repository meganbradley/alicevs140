---
title: "Property Get-Let-Set are no longer supported; use the new Property declaration syntax"
ms.custom: na
ms.date: 09/18/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - devlang-csharp
ms.tgt_pltfrm: na
ms.topic: article
H1: Property Get/Let/Set are no longer supported; use the new Property declaration syntax
ms.assetid: c8a803eb-316d-4f73-b6ef-27a2914409f3
caps.latest.revision: 12
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Property Get-Let-Set are no longer supported; use the new Property declaration syntax
`Property Get/Let/Set` are no longer supported; use the new `Property` declaration syntax.  
  
 The syntax for declaring properties has changed. Properties are now defined within blocks.  
  
 **Error ID:** BC30808  
  
### To correct this error  
  
1.  Define properties in blocks of code that begin with the `Property` keyword. End properties using the `End Property` construct.  
  
2.  Define `Get` property procedures within property blocks with the `Get` keyword. End `Get` property procedures with the `End Get` construct.  
  
3.  Define property `Set` procedures within property blocks with the `Set` keyword. End `Set` property procedures with the `End Set` construct.  
  
4.  Use `Set` property procedures for all property assignments. `Let` property procedures are no longer necessary, or supported.  
  
## See Also  
 [Property Statement](../vs140/Property-Statement.md)   
 [Language Changes for Visual Basic 6.0 Users](https://msdn.microsoft.com/en-us/library/skw8dhdd\(v=vs.90\).aspx)