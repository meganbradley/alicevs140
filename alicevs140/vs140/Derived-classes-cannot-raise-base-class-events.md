---
title: "Derived classes cannot raise base class events"
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
ms.assetid: 63afa1c6-2f93-4512-a2f0-372455979771
caps.latest.revision: 11
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Derived classes cannot raise base class events
An event can be raised only from the declaration space in which it is declared. Therefore, a class cannot raise events from any other class, even one from which it is derived.  
  
 **Error ID:** BC30029  
  
### To correct this error  
  
-   Move the `Event` statement or the `RaiseEvent` statement so they are in the same class.  
  
## See Also  
 [Event Statement](../vs140/Event-Statement.md)   
 [RaiseEvent Statement](../vs140/RaiseEvent-Statement.md)