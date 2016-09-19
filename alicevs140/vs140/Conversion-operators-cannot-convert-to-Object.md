---
title: "Conversion operators cannot convert to Object"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - devlang-csharp
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 064b478c-85a1-4e13-a292-d8aebb079cad
caps.latest.revision: 12
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Conversion operators cannot convert to Object
A conversion operator is declared with a return type of the [Object Data Type](../Topic/Object%20Data%20Type.md).  
  
 At compile time, [!INCLUDE[vbprvb](../vs140/includes/vbprvb_md.md)] considers a predefined conversion to exist from any reference type to any type in its inheritance hierarchy, that is, any type from which it derives or which derives from it. `Object` is the universal data type in the [!INCLUDE[dnprdnshort](../vs140/includes/dnprdnshort_md.md)], so every type derives from `Object`.  
  
 Because the compiler considers this conversion to be already defined, it does not allow you to redefine it.  
  
 **Error ID:** BC33028  
  
### To correct this error  
  
-   Remove this operator definition entirely. It is already predefined.  
  
## See Also  
 [Operator Procedures](../vs140/Operator-Procedures--Visual-Basic-.md)   
 [Operator Statement](../vs140/Operator-Statement.md)   
 [How to: Define an Operator](../vs140/How-to--Define-an-Operator--Visual-Basic-.md)   
 [How to: Define a Conversion Operator](../vs140/How-to--Define-a-Conversion-Operator--Visual-Basic-.md)   
 [Object as the Universal Data Type (Visual Basic)](assetId:///5315bf21-2b22-45ab-98cd-5631dffbcb2f)