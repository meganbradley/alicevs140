---
title: "Compiler Error CS0167"
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
ms.assetid: e6901b40-11a0-422c-9ea3-3b25c0ad7791
caps.latest.revision: 10
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Compiler Error CS0167
The delegate 'delegate' is missing the Invoke method  
  
 You imported and used a managed program (one that uses the .NET Framework common language runtime) that was created with another compiler. That compiler allowed an ill-formed [delegate](../vs140/delegate--C#-Reference-.md). Therefore, the `Invoke` method was not available. For more information, see [Delegates (C# Programmer's Reference)](../Topic/Delegates%20\(C%23%20Programming%20Guide\).md).