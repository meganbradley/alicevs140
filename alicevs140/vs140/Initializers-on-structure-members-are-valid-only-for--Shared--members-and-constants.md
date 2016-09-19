---
title: "Initializers on structure members are valid only for &#39;Shared&#39; members and constants"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - devlang-csharp
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 8356978e-7f84-4932-be0f-dda005c9f8ca
caps.latest.revision: 13
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Initializers on structure members are valid only for &#39;Shared&#39; members and constants
A structure member variable was initialized as part of its declaration.  
  
 **Error ID:** BC31049  
  
### To correct this error  
  
-   Use a constant instead of a variable.  
  
-   Add a parameterized constructor to the structure. For example:  
  
    ```  
    Structure TestStruct  
       Public t As Integer  
       Sub New(ByVal Tval As Integer)  
          t = Tval  
       End Sub  
    End Structure  
    ```  
  
## See Also  
 [How to: Declare a Structure](../vs140/How-to--Declare-a-Structure--Visual-Basic-.md)   
 [Constants and Enumerations](../vs140/Constants-and-Enumerations-in-Visual-Basic.md)