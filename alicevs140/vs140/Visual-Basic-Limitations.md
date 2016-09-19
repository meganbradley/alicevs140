---
title: "Visual Basic Limitations"
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
ms.assetid: cf1646b7-5d24-48c6-9616-bda8a4849d91
caps.latest.revision: 16
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Visual Basic Limitations
Earlier versions of [!INCLUDE[vbprvb](../vs140/includes/vbprvb_md.md)] enforced boundaries in code, such as the length of variable names, the number of variables allowed in modules, and module size. In [!INCLUDE[vbprvblong](../vs140/includes/vbprvblong_md.md)], these restrictions have been relaxed, giving you greater freedom in writing and arranging your code.  
  
 Physical limits are dependent more on run-time memory than on compile-time considerations. If you use prudent programming practices, and divide large applications into multiple classes and modules, then there is very little chance of encountering an internal [!INCLUDE[vbprvb](../vs140/includes/vbprvb_md.md)] limitation.  
  
 The following are some limitations that you might encounter in extreme cases:  
  
-   **Name Length.** There is a maximum number of characters for the name of every declared programming element. This maximum applies to an entire qualification string if the element name is qualified. See [Declared Element Names](../vs140/Declared-Element-Names--Visual-Basic-.md).  
  
-   **Line Length.** There is a maximum of 65535 characters in a physical line of source code. The logical source code line can be longer if you use line continuation characters. See [How to: Break and Combine Statements in Code](../vs140/How-to--Break-and-Combine-Statements-in-Code--Visual-Basic-.md).  
  
-   **Array Dimensions.** There is a maximum number of dimensions you can declare for an array. This limits how many indexes you can use to specify an array element. See [Array Dimensions in Visual Basic](../Topic/Array%20Dimensions%20in%20Visual%20Basic.md).  
  
-   **String Length.** There is a maximum number of Unicode characters you can store in a single string. See [String Data Type (Visual Basic)](../Topic/String%20Data%20Type%20\(Visual%20Basic\).md).  
  
-   **Environment String Length.** There is a maximum of 32768 characters for any environment string used as a command-line argument. This is a limitation on all platforms.  
  
## See Also  
 [Program Structure and Code Conventions](../vs140/Program-Structure-and-Code-Conventions--Visual-Basic-.md)   
 [Visual Basic Naming Conventions](../Topic/Visual%20Basic%20Naming%20Conventions.md)