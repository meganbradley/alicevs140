---
title: "Troubleshooting Code Analysis Issues"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - vs-ide-general
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 61c7e44d-2780-4df5-9bcb-49e40c1152fc
caps.latest.revision: 7
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Troubleshooting Code Analysis Issues
This topic contains troubleshooting information for the following Visual Studio code analysis issues.  
  
-   [Changes in a Visual Studio 2010 Rule Set Are Not Reflected in Previous Visual Studio Versions](#ChildRuleSetChangesInPreviousVersions)  
  
##  <a name="ChildRuleSetChangesInPreviousVersions"></a> Changes in a Visual Studio 2010 Rule Set Are Not Reflected in Previous Visual Studio Versions  
 When you create a rule set in [!INCLUDE[vs_dev10_long](../vs140/includes/vs_dev10_long_md.md)] that contains a child rule set, a change to the child rule set might not be applied in code analysis runs on computers that use an earlier version of Visual Studio. To resolve this issue, you must force a rewrite of the parent rule set, that is the rule set that contains the child rule set.  
  
1.  Open the parent rule set in [!INCLUDE[vs_dev10_long](../vs140/includes/vs_dev10_long_md.md)].  
  
2.  Make a change, such as adding or removing a rule, and then save the rule set.  
  
3.  Reopen the rule set, reverse the change, and then save the rule set again.  
  
## See Also  
 [Analyzing Application Quality by Using Code Analysis Tools](../vs140/Analyzing-Application-Quality-by-Using-Code-Analysis-Tools.md)   
 [Analyzing Managed Code Quality By Using Code Analysis](../vs140/Analyzing-Managed-Code-Quality-by-Using-Code-Analysis.md)   
 [Using Rule Sets to Specify Managed Code Analysis Rules](../vs140/Using-Rule-Sets-to-Group-Code-Analysis-Rules.md)