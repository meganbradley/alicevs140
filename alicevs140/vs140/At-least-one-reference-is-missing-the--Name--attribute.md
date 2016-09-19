---
title: "At least one reference is missing the &#39;Name&#39; attribute"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - devlang-csharp
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 0703dc20-9cdd-4632-93a0-57a4ccea2fce
caps.latest.revision: 9
translation.priority.ht: 
  - de-de
  - ja-jp
---
# At least one reference is missing the &#39;Name&#39; attribute
Each reference must have an associated **Name** property, as seen below:  
  
```  
<Reference  
   Name = "System.XML"  
   AssemblyName = "System.Xml"  
/>  
```  
  
 This error indicates that the **Name** property was not found for at least one reference.  
  
 This error is most likely caused by editing the project file by hand.  
  
 **To correct this error**  
  
-   Add the reference again.  
  
     Any affected references will not be added to the project.  
  
## See Also  
 [NIB How to: Add or Remove References By Using the Add Reference Dialog Box](assetId:///3bd75d61-f00c-47c0-86a2-dd1f20e231c9)   
 [Managing references in a project](../Topic/Managing%20references%20in%20a%20project.md)