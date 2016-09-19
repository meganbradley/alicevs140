---
title: "MSBuild Error MSB1024"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - devlang-csharp
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: dff30870-da1a-479f-998b-03d0f5e16088
caps.latest.revision: 9
translation.priority.ht: 
  - de-de
  - ja-jp
---
# MSBuild Error MSB1024
**Only one schema can be specified for validation of the project.**  
  
 Only one schema can be specified for the **/validate** switch.  
  
### To correct this error  
  
1.  Specify only one schema to validate the project against using the format `/validate:<schema>`, for example, `/validate:MyExtendedBuildSchema.xsd`  
  
## See Also  
 [MSBuild Command Line Reference](../vs140/MSBuild-Command-Line-Reference.md)