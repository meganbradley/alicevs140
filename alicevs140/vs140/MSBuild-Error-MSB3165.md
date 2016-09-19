---
title: "MSBuild Error MSB3165"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - devlang-csharp
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 2f50462e-947d-4211-b197-e58eddcfd373
caps.latest.revision: 8
translation.priority.ht: 
  - de-de
  - ja-jp
---
# MSBuild Error MSB3165
**MSB3165: The value of the '<public key\>' attribute in '<package\>' does not match that of file '<file\>'.**  
  
 This warning occurs when the public key specified in the bootstrapper package file does not match the signature of the redistributable package on disk, or the redistributable package is not signed. The build will take the public key value of that on disk if it is signed, or take the hash of the redistributable package on disk if it is not signed.  
  
## See Also  
 [<PackageFiles\> Element (ClickOnce Bootstrapper)](../vs140/-PackageFiles--Element--Bootstrapper-.md)   
 [Product and Package Schema Reference](../vs140/Product-and-Package-Schema-Reference.md)