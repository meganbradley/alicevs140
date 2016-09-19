---
title: "MSBuild Error MSB1004"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - devlang-csharp
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: aed36761-ab07-486c-b5eb-48ccb1c387dd
caps.latest.revision: 14
translation.priority.ht: 
  - de-de
  - ja-jp
---
# MSBuild Error MSB1004
**Specify the name of the target.**  
  
 At least one target must be specified with the **/target** switch.  
  
### To correct this error  
  
1.  Specify a target or targets. You can use either a comma or a semicolon to separate a list of targets, for example, `/target:Clean;Compile`. Alternatively, you can repeat the switch, for example, `/t:Clean /t:``Compile`  
  
## See Also  
 [MSBuild Targets](../vs140/MSBuild-Targets.md)   
 [MSBuild Command Line Reference](../vs140/MSBuild-Command-Line-Reference.md)