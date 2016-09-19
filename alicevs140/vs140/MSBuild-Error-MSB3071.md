---
title: "MSBuild Error MSB3071"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - devlang-csharp
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 8afbc6ec-e399-4f06-a30b-f33c87642ef7
caps.latest.revision: 10
translation.priority.ht: 
  - de-de
  - ja-jp
---
# MSBuild Error MSB3071
**All drive letters from A: to Z: are currently in use. Since the working directory "'<path\>'" is a UNC path, The "Exec" task needs a free drive letter to map the UNC path to. Disconnect from one or more shared resources to free up drive letters, or specify a local working directory before attempting this command again.**  
  
 All drive letters from A: through Z: are currently in use. Because the specified working directory is a UNC path, the `Exec` task needs a free drive letter to which to map the UNC path to.  
  
### To correct this error  
  
-   Disconnect from one or more shared resources to free drive letters  
  
-   Specify a local working directory before attempting this command again.  
  
## See Also  
 [Exec Task](../Topic/Exec%20Task.md)