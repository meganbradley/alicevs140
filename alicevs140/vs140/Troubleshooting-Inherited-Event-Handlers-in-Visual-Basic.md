---
title: "Troubleshooting Inherited Event Handlers in Visual Basic"
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
ms.assetid: e1c8759f-5370-4308-8476-8c48b73509bf
caps.latest.revision: 13
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Troubleshooting Inherited Event Handlers in Visual Basic
This topic lists common issues that arise with event handlers in inherited components.  
  
## Procedures  
  
#### Code in Event Handler Executes Twice for Every Call  
  
-   An inherited event handler must not include a [Handles](../vs140/Handles-Clause--Visual-Basic-.md) clause. The method in the base class is already associated with the event and will fire accordingly. Remove the `Handles` clause from the inherited method.  
  
     [!CODE [VbVbalrEvents#32](../CodeSnippet/VS_Snippets_VBCSharp/VbVbalrEvents#32)]  
  
-   If the inherited method does not have a `Handles` keyword, verify that your code does not contain an extra [AddHandler Statement](../vs140/AddHandler-Statement.md) or any additional methods that handle the same event.  
  
## See Also  
 [Events (Visual Basic)](../vs140/Events--Visual-Basic-.md)