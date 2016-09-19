---
title: "MSBuild Error MSB1027"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - devlang-csharp
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 2ef8d643-616c-4608-be76-5c2c8e18a9e7
caps.latest.revision: 6
translation.priority.ht: 
  - de-de
  - ja-jp
---
# MSBuild Error MSB1027
**The /noautoresponse switch cannot be specified in the MSBuild.rsp auto-response file, nor in any response file that is referenced by the auto-response file.**  
  
 The **/noautoresponse** switch was found inside either the MSBuild.rsp file, or in another response file included by the MSBuild.rsp file. The auto-response file cannot be used to turn itself off.  
  
### To correct this error  
  
-   Specify a different response file  
  
-   Remove the **/noautoresponse** switch from the MSBuild.rsp response file.  
  
## See Also  
 [MSBuild Command Line Reference](../vs140/MSBuild-Command-Line-Reference.md)