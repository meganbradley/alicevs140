---
title: "MSBuild Error MSB3144"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - devlang-csharp
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 955e0db3-afe2-4c03-8e95-3419878374df
caps.latest.revision: 7
translation.priority.ht: 
  - de-de
  - ja-jp
---
# MSBuild Error MSB3144
**MSB3144: Not enough data was provided to generate a bootstrapper. Please provide a value for at least one of the parameters: 'ApplicationFile' or 'BootstrapperItems'."**  
  
 This error occurs when not enough data has been provided to generate a bootstrapper. The build process creates an empty bootstrapper with no application installer and no packages.  
  
### To correct this error  
  
-   Provide a value for at least one of the parameters `ApplicationFile` or `BootstrapperItems`.  
  
## See Also  
 [Product and Package Schema Reference](../vs140/Product-and-Package-Schema-Reference.md)