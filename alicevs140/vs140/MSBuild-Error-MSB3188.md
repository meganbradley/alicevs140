---
title: "MSBuild Error MSB3188"
ms.custom: na
ms.date: 09/18/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - devlang-csharp
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 8520e960-3b31-4e25-9fce-b9092b869bd0
caps.latest.revision: 7
translation.priority.ht: 
  - de-de
  - ja-jp
---
# MSBuild Error MSB3188
**MSB3188: Assembly '<assembly\>' must be strong signed in order to be marked as a prerequisite.**  
  
 This error is generated when a prerequisite assembly is not strong-signed. It applies only to application manifests.  
  
### To correct this error  
  
-   Ensure that all assemblies that the project uses are strong-signed.