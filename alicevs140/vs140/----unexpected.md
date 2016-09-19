---
title: "&#39;(&#39; unexpected"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - devlang-csharp
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: a47ad15a-2cfc-4d17-9012-27ba85b7d783
caps.latest.revision: 10
translation.priority.ht: 
  - de-de
  - ja-jp
---
# &#39;(&#39; unexpected
'(' unexpected. Arrays of uninstantiated generic types are not allowed.  
  
 [!INCLUDE[vbprvb](../vs140/includes/vbprvb_md.md)] cannot compile an array unless it is of a specific data type. You cannot use a data-type parameter of a generic type as the data type of an array.  
  
 **Error ID:** BC32095  
  
### To correct this error  
  
-   If you need to use an array, you must declare it to be of a specific data type. You cannot use a data-type parameter.  
  
-   If you need a group of elements of the data type that is to be supplied for a data-type parameter, you must use a collection instead of an array.  
  
## See Also  
 [Generic Types in Visual Basic](../Topic/Generic%20Types%20in%20Visual%20Basic%20\(Visual%20Basic\).md)   
 [NIB Collections in Visual Basic](assetId:///8b2b7845-2251-4573-8dd3-c9f9c0a66a21)   
 [Managing Groups of Objects in Visual Basic](assetId:///50be4910-4732-4d5f-a18a-055a162e9037)