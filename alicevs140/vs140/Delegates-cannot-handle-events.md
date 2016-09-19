---
title: "Delegates cannot handle events"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - devlang-csharp
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 7f0c7bb9-8e81-44bf-acc5-80d9785708aa
caps.latest.revision: 10
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Delegates cannot handle events
A delegate is a reference type that points to a shared procedure or to an instance procedure on an object. Because the procedure it points to can be changed by assignment, the `Delegate` statement cannot support the `Handles` or `Implements` clauses.  
  
 **Error ID:** BC30019  
  
### To correct this error  
  
-   Remove the `Handles` clause from the `Delegate` statement.  
  
## See Also  
 [NOT IN BUILD: Delegates and the AddressOf Operator](assetId:///7b2ed932-8598-4355-b2f7-5cedb23ee86f)   
 [Delegate Statement](../vs140/Delegate-Statement.md)   
 [Handles](../vs140/Handles-Clause--Visual-Basic-.md)   
 [Implements Statement](../vs140/Implements-Statement.md)