---
title: "Optional parameters must specify a default value"
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
ms.assetid: 5091a250-be66-413b-98a3-2a9974c4d600
caps.latest.revision: 12
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Optional parameters must specify a default value
Optional parameters must provide default values that can be used if no parameter is supplied by a calling procedure.  
  
 **Error ID:** BC30812  
  
### To correct this error  
  
-   Specify default values for optional parameters; for example:  
  
    ```  
    Sub Proc1(ByVal X As Integer,   
          Optional ByVal Y As String = "Default Value")  
       MsgBox("Default argument is: " & Y)  
    End Sub  
    ```  
  
## See Also  
 [Optional](../vs140/Optional--Visual-Basic-.md)