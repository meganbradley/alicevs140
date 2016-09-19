---
title: "Referenced object has a value of &#39;Nothing&#39;"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - devlang-csharp
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 7e792fd8-2880-402b-a908-c89e5b028300
caps.latest.revision: 10
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Referenced object has a value of &#39;Nothing&#39;
The object being used has the value `Nothing`, but a usable value is expected. `Nothing` is a value that indicates that an object has no value, either because no value has been assigned to it, or it was assigned the value `Nothing`.  
  
 **Error ID:** BC30760  
  
### To correct this error  
  
1.  Check the object to make sure it has been declared within the scope of the procedure where the error occurred.  
  
2.  Verify that the value of the object is being set.  
  
    > [!NOTE]
    >  The value `Nothing` is not the same as zero or an empty string. You can use `IsNothing` to check to see if an object contains the value `Nothing`.  
  
## See Also  
 [Nothing](../Topic/Nothing%20\(Visual%20Basic\).md)   
 [NOT IN BUILD: IsNothing Function](assetId:///5b2a4626-e6a9-49d1-b9b1-fcc6a1302319)