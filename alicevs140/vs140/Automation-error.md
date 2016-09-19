---
title: "Automation error"
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
ms.assetid: 2c4be5c5-2f0d-4a2b-96fe-d1b24f08fc4c
caps.latest.revision: 11
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Automation error
An error occurred while executing a method or getting or setting a property of an object variable. The error was reported by the application that created the object.  
  
### To correct this error  
  
1.  Check the properties of the `Err` object to determine the source and nature of the error.  
  
2.  Use the `On Error Resume Next` statement immediately before the accessing statement, and then check for errors immediately after the accessing statement.  
  
## See Also  
 [Types of Errors](../vs140/Error-Types--Visual-Basic-.md)   
 [Getting Assistance](../vs140/Talk-to-Us.md)