---
title: "MSBuild Best Practices"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - vs-ide-sdk
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 90ef8693-e921-410a-a377-fe4d13f58c48
caps.latest.revision: 7
translation.priority.ht: 
  - de-de
  - ja-jp
---
# MSBuild Best Practices
We recommend the following best practices for writing MSBuild scripts:  
  
-   Default property values are best handled by using the `Condition` attribute, and not by declaring a property whose default value can be overridden on the command line. For example, use  
  
     `<MyProperty Condition="$(MyProperty)" == ''>`  
  
     `MyDefaultValue`  
  
     `</MyProperty>`  
  
-   Avoid wildcards when you select items. Instead, specify files explicitly. This makes it easier to track down errors that may occur when you add or delete files.  
  
## See Also  
 [MSBuild Advanced Concepts](../vs140/MSBuild-Advanced-Concepts.md)