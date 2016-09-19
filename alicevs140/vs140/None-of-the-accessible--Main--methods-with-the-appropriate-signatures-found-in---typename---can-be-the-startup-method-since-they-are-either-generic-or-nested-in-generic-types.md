---
title: "None of the accessible &#39;Main&#39; methods with the appropriate signatures found in &#39;&lt;typename&gt;&#39; can be the startup method since they are either generic or nested in generic types"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - devlang-csharp
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 606b3629-5a92-4c79-ace2-a530cab8c978
caps.latest.revision: 14
translation.priority.ht: 
  - de-de
  - ja-jp
---
# None of the accessible &#39;Main&#39; methods with the appropriate signatures found in &#39;&lt;typename&gt;&#39; can be the startup method since they are either generic or nested in generic types
A class, module, or structure does not have any `Main` procedure that qualifies as the project startup procedure.  
  
 Visual Basic requires that the startup procedure for a project must not be dependent on type arguments. Therefore, it must be able to access at least one `Main` procedure that is neither generic nor contained in any generic type.  
  
 **Error ID:** BC30796  
  
### To correct this error  
  
-   Define at least one of the `Main` procedures so that it is not generic and is not contained in a generic type.  
  
     -or-  
  
-   On the **Properties** page for your project, specify a different form or module for the **Startup form** or **Startup object**.  
  
## See Also  
 [NIB How to: Modify Project Properties and Configuration Settings](assetId:///e7184bc5-2f2b-4b4f-aa9a-3ecfcbc48b67)   
 [Generic Types in Visual Basic](../Topic/Generic%20Types%20in%20Visual%20Basic%20\(Visual%20Basic\).md)   
 [NIB: Visual Basic Version of Hello, World](assetId:///9d030b60-e148-4366-a462-69532f02294c)