---
title: "Structures cannot declare a non-shared &#39;Sub New&#39; with no parameters"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - devlang-csharp
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: f4298ef7-85b1-4543-b764-4c3abda84baa
caps.latest.revision: 10
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Structures cannot declare a non-shared &#39;Sub New&#39; with no parameters
`Sub New` constructors declared within structures must either accept arguments or be declared with the `Shared` modifier.  
  
 **Error ID:** BC30629  
  
### To correct this error  
  
-   Change the `Sub New` constructor so that it accepts arguments.  
  
-   Apply the `Shared` modifier to make the constructor shared.  
  
## See Also  
 [Structure Statement](../Topic/Structure%20Statement.md)   
 [Structures](../vs140/Structures--Visual-Basic-.md)