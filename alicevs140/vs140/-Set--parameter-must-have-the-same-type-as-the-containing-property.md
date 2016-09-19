---
title: "&#39;Set&#39; parameter must have the same type as the containing property"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - devlang-csharp
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: f0b8310d-68a1-4989-ac64-03b1861528ad
caps.latest.revision: 10
translation.priority.ht: 
  - de-de
  - ja-jp
---
# &#39;Set&#39; parameter must have the same type as the containing property
The parameter for the `Set` property procedure has a different type from the property that it belongs to.  
  
 **Error ID:** BC31064  
  
### To correct this error  
  
-   Change the data type of the parameter to `Set` so that it matches the data type for the property. For example:  
  
    ```  
    Class Class1  
       ' Declare a local variable to hold the property value.  
       Private Fval As Integer  
  
       Property F() As Integer  
          Get  
             Return Fval  
          End Get  
          Set(ByVal Value As Integer)  
             Fval = Value  
          End Set  
       End Property  
    End Class  
    ```  
  
## See Also  
 [NOT IN BUILD: How to: Add Fields and Properties to a Class](assetId:///ae53f61b-3abc-413e-8931-703c5f5e8fc2)   
 [Property Procedures](../vs140/Property-Procedures--Visual-Basic-.md)   
 [NOT IN BUILD: Properties and Property Procedures](assetId:///23e2a1ec-7e9d-4109-8940-c703d981077b)