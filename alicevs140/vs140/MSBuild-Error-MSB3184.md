---
title: "MSBuild Error MSB3184"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - devlang-csharp
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 2be9f8e9-04ee-4299-b79f-965ee57a1a34
caps.latest.revision: 7
translation.priority.ht: 
  - de-de
  - ja-jp
---
# MSBuild Error MSB3184
**MSB3184: Input manifest is invalid.**  
  
 This error is generated when the build process tries to load a file, expecting that it contains either an application manifest or a deployment manifest, but it turns out to contain something else (such as a different manifest or corrupt data).  
  
### To correct this error  
  
-   Verify that the manifests in your project are valid and appropriate.  
  
## See Also  
 [<PackageFiles\> Element (ClickOnce Bootstrapper)](../vs140/-PackageFiles--Element--Bootstrapper-.md)