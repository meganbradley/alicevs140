---
title: "MSBuild Error MSB3154"
ms.custom: na
ms.date: 09/18/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - devlang-csharp
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 513b70fa-15f5-4137-bdbc-5974607fb75a
caps.latest.revision: 8
translation.priority.ht: 
  - de-de
  - ja-jp
---
# MSBuild Error MSB3154
**MSB3154: Could not find string resources for item '<package\>'.**  
  
 This error is generated when the specified package does not contain any culture-specific information. Either a package.xml file does not exist, or it does not contain a `Culture` attribute.  
  
### To correct this error  
  
-   Provide a valid package.xml that contains a correct `Culture` tag.