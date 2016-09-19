---
title: "&#39;Exit Operator&#39; is not valid. Use &#39;Return&#39; to exit an Operator"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - devlang-csharp
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 8c44456b-8fd2-4168-ad8c-b6da129242ba
caps.latest.revision: 10
translation.priority.ht: 
  - de-de
  - ja-jp
---
# &#39;Exit Operator&#39; is not valid. Use &#39;Return&#39; to exit an Operator
An `Exit Operator` statement appears in an `Operator` procedure.  
  
 You must use a [Return Statement (Visual Basic)](../vs140/Return-Statement--Visual-Basic-.md) to return from an `Operator` procedure. The [Exit Statement (Visual Basic)](../vs140/Exit-Statement--Visual-Basic-.md) does not accept the `Operator` keyword, and the `End Operator` statement does not return control to the calling code.  
  
 **Error ID:** BC33008  
  
### To correct this error  
  
-   Replace the `Exit Operator` statement with a `Return` statement.  
  
## See Also  
 [Operator Procedures](../vs140/Operator-Procedures--Visual-Basic-.md)   
 [Operator Statement](../vs140/Operator-Statement.md)   
 [How to: Define an Operator](../vs140/How-to--Define-an-Operator--Visual-Basic-.md)   
 [How to: Define a Conversion Operator](../vs140/How-to--Define-a-Conversion-Operator--Visual-Basic-.md)