---
title: "MSBuild Error MSB3072"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - devlang-csharp
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: c8468e1c-d8c7-441c-b274-123ac856f147
caps.latest.revision: 8
translation.priority.ht: 
  - de-de
  - ja-jp
---
# MSBuild Error MSB3072
**The "Exec" task needs a command to execute.**  
  
 The attribute `Command` is a required attribute for the `Exec` task.  
  
### To correct this error  
  
1.  In the project file, specify the attribute `Command` for the `Exec` task.  
  
## See Also  
 [Exec Task](../Topic/Exec%20Task.md)   
 [MSBuild Tasks](../Topic/MSBuild%20Tasks.md)