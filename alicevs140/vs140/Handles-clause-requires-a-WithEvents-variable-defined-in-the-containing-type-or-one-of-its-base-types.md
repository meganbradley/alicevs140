---
title: "Handles clause requires a WithEvents variable defined in the containing type or one of its base types"
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
ms.assetid: 5b66f6a8-f050-4e03-a57f-a64e85f80cb5
caps.latest.revision: 13
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Handles clause requires a WithEvents variable defined in the containing type or one of its base types
You did not supply a `WithEvents` variable in your `Handles` clause. The `Handles` keyword at the end of a procedure declaration causes it to handle events raised by an object variable declared using the `WithEvents` keyword.  
  
 **Error ID:** BC30506  
  
### To correct this error  
  
-   Supply the necessary `WithEvents` variable.  
  
## See Also  
 [Handles](../vs140/Handles-Clause--Visual-Basic-.md)