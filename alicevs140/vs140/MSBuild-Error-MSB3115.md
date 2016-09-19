---
title: "MSBuild Error MSB3115"
ms.custom: na
ms.date: 09/18/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - devlang-csharp
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 7d9d4156-fd6a-455a-8a3d-b191485f1294
caps.latest.revision: 7
translation.priority.ht: 
  - de-de
  - ja-jp
---
# MSBuild Error MSB3115
**MSB3115: File '<file\>' is not a valid entry point.**  
  
 This error is generated when a manifest specifies an entry point that is not valid.  
  
### To correct this error  
  
-   Be sure that you specify valid entry points in your manifests. For an application manifest, a valid entry point is an .exe file. For a deployment manifest, a valid entry point is an application manifest.