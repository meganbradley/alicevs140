---
title: "Type characters cannot be used in anonymous type declarations"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - devlang-csharp
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 70eee559-d6fc-409b-b835-2c84511b160e
caps.latest.revision: 13
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Type characters cannot be used in anonymous type declarations
You cannot use a type character on a property name when you declare an instance of an anonymous type. The data type of the property is inferred from the value assigned to it. For example, the following declarations are not valid.  
  
```vb#  
'' Not valid.  
'Dim anon1 = New With {.ID$ = "abc"}  
'Dim anon2 = New With {.ID$ = 42}  
```  
  
 **Error ID:** BC36560  
  
### To correct this error  
  
-   Remove the type character from the initializer list. You can explicitly convert the assigned value if this is necessary to establish the data type you want for the property.  
  
    ```vb#  
    ' Valid.  
    Dim anon1 = New With {.ID = "abc"}  
    Dim anon2 = New With {.ID = CStr(42)}  
    ```  
  
## See Also  
 [Anonymous Types](../Topic/Anonymous%20Types%20\(Visual%20Basic\).md)   
 [How to: Infer Property Names and Types in Anonymous Type Declarations](../vs140/How-to--Infer-Property-Names-and-Types-in-Anonymous-Type-Declarations--Visual-Basic-.md)   
 [Implicit and Explicit Conversions](../Topic/Implicit%20and%20Explicit%20Conversions%20\(Visual%20Basic\).md)