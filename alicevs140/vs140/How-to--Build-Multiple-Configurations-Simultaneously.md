---
title: "How to: Build Multiple Configurations Simultaneously"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - vs-ide-general
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: ba830937-3317-4674-8cc2-c0cd565603c5
caps.latest.revision: 12
translation.priority.ht: 
  - de-de
  - ja-jp
---
# How to: Build Multiple Configurations Simultaneously
You can build most types of projects with multiple, or even all, of their build configurations at the same time by using the **Batch Build** dialog box. However, you can't build the following types of projects in multiple build configurations at the same time:  
  
1.  [!INCLUDE[win8_appname_long](../vs140/includes/win8_appname_long_md.md)] apps built for Windows using JavaScript.  
  
2.  All Visual Basic projects.  
  
 For more information about build configurations, see [Understanding Build Configurations](../vs140/Understanding-Build-Configurations.md).  
  
### To build a project in multiple build configurations  
  
1.  On the menu bar, choose **Build**, **Batch Build**.  
  
2.  In the **Build** column, select the check boxes for the configurations in which you want to build a project.  
  
    > [!TIP]
    >  To edit or create a build configuration for a solution, choose **Build**, **Configuration Manager** on the menu bar to open the **Configuration Manager** dialog box. After you have edited a build configuration for a solution, choose the **Rebuild** button in the **Batch Build** dialog box to update all build configurations for the projects in the solution.  
  
3.  Choose the **Build** or **Rebuild** buttons to build the project with the configurations that you specified.  
  
## See Also  
 [How to: Create and Edit Configurations](../vs140/How-to--Create-and-Edit-Configurations.md)   
 [Build Configurations](../vs140/Understanding-Build-Configurations.md)   
 [Building Multiple Projects in Parallel](../Topic/Building%20Multiple%20Projects%20in%20Parallel%20with%20MSBuild.md)