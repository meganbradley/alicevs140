---
title: "Class does not support Automation or does not support expected interface"
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
ms.assetid: d985bb7e-e48e-443e-86f2-ddb86758757c
caps.latest.revision: 13
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Class does not support Automation or does not support expected interface
Either the class you specified in the `GetObject` or `CreateObject` function call has not exposed a programmability interface, or you changed a project from .dll to .exe, or vice versa.  
  
### To correct this error  
  
1.  Check the documentation of the application that created the object for limitations on the use of automation with this class of object.  
  
2.  If you changed a project from .dll to .exe or vice versa, you must manually unregister the old .dll or .exe.  
  
## See Also  
 [Types of Errors](../vs140/Error-Types--Visual-Basic-.md)   
 [Product Support and Accessibility](../vs140/Talk-to-Us.md)