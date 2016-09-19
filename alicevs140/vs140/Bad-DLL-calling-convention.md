---
title: "Bad DLL calling convention"
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
ms.assetid: 7c7def45-b0ab-450f-ad3f-4383dfd9aed7
caps.latest.revision: 10
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Bad DLL calling convention
Arguments passed to a dynamic-link library (DLL) must exactly match those expected by the routine. Calling conventions deal with number, type, and order of arguments. Your program may be calling a routine in a DLL that is being passed the wrong type or number of arguments.  
  
### To correct this error  
  
1.  Make sure all argument types agree with those specified in the declaration of the routine that you are calling.  
  
2.  Make sure you are passing the same number of arguments indicated in the declaration of the routine that you are calling.  
  
3.  If the DLL routine expects arguments by value, make sure `ByVal` is specified for those arguments in the declaration for the routine.  
  
## See Also  
 [Types of Errors](../vs140/Error-Types--Visual-Basic-.md)   
 [Call Statement](../vs140/Call-Statement--Visual-Basic-.md)   
 [Declare Statement](../Topic/Declare%20Statement.md)