---
title: "Conversion operators cannot convert from an interface type"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - devlang-csharp
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 0d0ee461-dd48-424b-b83a-484bfc648d4d
caps.latest.revision: 12
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Conversion operators cannot convert from an interface type
A conversion operator is declared with an interface type for the parameter.  
  
 At compile time, [!INCLUDE[vbprvb](../vs140/includes/vbprvb_md.md)] considers a predefined conversion to exist from any interface to any reference type. Such a conversion might fail at run time, but the compiler cannot predict run-time results, so it allows any such conversion to compile.  
  
 Because the compiler considers this conversion to be already defined, it does not allow you to redefine it.  
  
 **Error ID:** BC33029  
  
### To correct this error  
  
-   Remove this operator definition entirely. It is already predefined.  
  
## See Also  
 [Operator Procedures](../vs140/Operator-Procedures--Visual-Basic-.md)   
 [Operator Statement](../vs140/Operator-Statement.md)   
 [How to: Define an Operator](../vs140/How-to--Define-an-Operator--Visual-Basic-.md)   
 [How to: Define a Conversion Operator](../vs140/How-to--Define-a-Conversion-Operator--Visual-Basic-.md)