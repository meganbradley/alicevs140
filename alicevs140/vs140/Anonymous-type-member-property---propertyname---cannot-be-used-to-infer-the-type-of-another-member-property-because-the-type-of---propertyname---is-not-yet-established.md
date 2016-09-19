---
title: "Anonymous type member property &#39;&lt;propertyname&gt;&#39; cannot be used to infer the type of another member property because the type of &#39;&lt;propertyname&gt;&#39; is not yet established"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - devlang-csharp
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 58ab8d35-9d85-4aca-8b4e-f232d7e4af61
caps.latest.revision: 8
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Anonymous type member property &#39;&lt;propertyname&gt;&#39; cannot be used to infer the type of another member property because the type of &#39;&lt;propertyname&gt;&#39; is not yet established
Until the type of an anonymous type property is established, it cannot be used to establish the type of another property. For example, in the following declaration `.IDName = .LastName` is not valid because `.LastName` has not yet been initialized.  
  
```  
' Not valid.   
' Dim anon1 = New With {Key .IDName = .LastName, Key .LastName = "Jones"}   
```  
  
 **Error ID:** BC36559  
  
### To correct this error  
  
-   Establish the type of the property before using it to initialize another property.  
  
    ```  
    Dim anon2 = New With {Key .LastName = "Jones", Key .IDName = .LastName}  
    ```  
  
## See Also  
 [Anonymous Types](../Topic/Anonymous%20Types%20\(Visual%20Basic\).md)   
 [How to: Infer Property Names and Types in Anonymous Type Declarations](../vs140/How-to--Infer-Property-Names-and-Types-in-Anonymous-Type-Declarations--Visual-Basic-.md)