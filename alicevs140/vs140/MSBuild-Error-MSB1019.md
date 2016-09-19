---
title: "MSBuild Error MSB1019"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - devlang-csharp
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 5d0169f7-f878-433a-ac30-d9d6010130af
caps.latest.revision: 9
translation.priority.ht: 
  - de-de
  - ja-jp
---
# MSBuild Error MSB1019
**Logger switch was not correctly formed.**  
  
 The **/logger** switch is not correctly specified. To specify a logger, you must provide at least the logger assembly, or if you want to be explicitly specify which logger to load, provide both the logger class and the logger assembly. Logger parameters are optional.  
  
### To correct this error  
  
1.  Specify a logger using both the logger class and logger assembly. The `<logger>` syntax is:  
  
     `<logger class>,<logger assembly>[;<logger parameters>]`  
  
     The `<logger class>` syntax is:  
  
    ```  
    [<partial or full namespace>.]<logger class name>  
    ```  
  
     The `<logger assembly>`syntax is:  
  
    ```  
    {<assembly name>[,<strong name>] | <assembly file>}  
    ```  
  
     The `<logger parameters>` are optional and are passed to the logger exactly as you typed them.  
  
     Example: /`logger:XMLLogger,MyLogger,Version=1.0.2,Culture=neutral`  
  
## See Also  
 [MSBuild Command Line Reference](../vs140/MSBuild-Command-Line-Reference.md)   
 [How To: Write a Logger](../Topic/Build%20Loggers.md)