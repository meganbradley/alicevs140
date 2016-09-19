---
title: "MSBuild Error MSB3153"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - devlang-csharp
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 937bb1ff-79f7-45a5-a085-525f4b48ea4e
caps.latest.revision: 8
translation.priority.ht: 
  - de-de
  - ja-jp
---
# MSBuild Error MSB3153
**MSB3153: Xml validation did not pass for item '<package\>' located at '<folder\>'.**  
  
 This warning is generated when the manifest (specifically package.xml) does not pass XML validation. The specific problems are listed in a subsequent error message ([MSBuild Error MSB3159](../vs140/MSBuild-Error-MSB3159.md) or [MSBuild Error MSB3160](../vs140/MSBuild-Error-MSB3160.md)).  
  
### To correct this error  
  
-   Resolve the manifest validation issues listed in the subsequent error messages.  
  
## See Also  
 [Product and Package Schema Reference](../vs140/Product-and-Package-Schema-Reference.md)   
 [<PackageFiles\> Element (ClickOnce Bootstrapper)](../vs140/-PackageFiles--Element--Bootstrapper-.md)