---
title: "Methods declared in structures cannot have &#39;Handles&#39; clauses"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - devlang-csharp
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 64c70bb5-3696-4865-8194-328394c2b4b1
caps.latest.revision: 12
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Methods declared in structures cannot have &#39;Handles&#39; clauses
Structure methods cannot use the `Handles` keyword to handle events.  
  
 **Error ID:** BC30728  
  
### To correct this error  
  
-   Consider redesigning your structure as a class.  
  
     You can use `AddHandler` to associate an event with an event handler in a structure, provided that the structure implements an event handler defined in an interface.  
  
## See Also  
 [Structures and Classes](../Topic/Structures%20and%20Classes%20\(Visual%20Basic\).md)   
 [NOT IN BUILD: Classes: Blueprints for Objects](assetId:///2c86373d-0333-4616-a7d8-4790c4e89f7b)   
 [Events in Visual Basic](../vs140/Events--Visual-Basic-.md)   
 [NOT IN BUILD:AddHandler and RemoveHandler](assetId:///a7a24bd2-519a-46fe-8a2c-2b9df2ca28ef)