---
title: "MSBuild Error MSB3148"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - devlang-csharp
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 389b335f-5760-4dcc-9146-c52d6d7ac81f
caps.latest.revision: 8
translation.priority.ht: 
  - de-de
  - ja-jp
---
# MSBuild Error MSB3148
**MSB3148: No output path specified in build settings.**  
  
 This error occurs when a null or invalid output path is specified; for example, if `OutputPath=""` in the project file. The default value for the output path is `CurrentDirectory`.  
  
### To correct this error  
  
-   Make sure that `OutputPath` is not blank, or that it is not included in the project file.  
  
## See Also  
 [Product and Package Schema Reference](../vs140/Product-and-Package-Schema-Reference.md)