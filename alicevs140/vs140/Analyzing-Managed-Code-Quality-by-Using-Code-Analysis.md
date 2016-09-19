---
title: "Analyzing Managed Code Quality by Using Code Analysis"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - vs-ide-general
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 68510a55-da51-4381-81a5-0feba76b8b4f
caps.latest.revision: 26
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Analyzing Managed Code Quality by Using Code Analysis
You can use the code analysis tools in Visual Studio to discover potential issues in your code, such as non-secure data access, usage violations, and design problems. Code analysis works on .NET Framework, native (C and C++), and database applications. Code analysis for managed code organizes rules in *rule sets* that target specific coding issues.  
  
## Common Tasks  
  
|Common Tasks|Supporting Content|  
|------------------|------------------------|  
|**Get hands-on practice:** Learn the basics of code analysis by correcting defects in a simple .NET Framework application.|-   [Walkthrough: Analyzing Managed Code for Code Defects](../vs140/Walkthrough--Analyzing-Managed-Code-for-Code-Defects.md)|  
|**Configure code analysis for a project:** Rules for managed code are organized into rule sets that target specific areas, such as security and design. You can use one of the Microsoft standard rule sets or create your own.|-   [Code Analysis for Managed Code Overview](../vs140/Code-Analysis-for-Managed-Code-Overview.md)<br />-   [Using Rule Sets to Specify Managed Code Analysis Rules](../vs140/Using-Rule-Sets-to-Group-Code-Analysis-Rules.md)<br />-   [Suppress Warnings Using SuppressMessage Attribute](../vs140/Suppress-Warnings-By-Using-the-SuppressMessage-Attribute.md)|  
|**Run code analysis:** You can specify code analysis to be run automatically every time that a project configuration is built, and you can run code analysis manually on a project.|-   [How to: Enable and Disable Automatic Code Analysis for Managed Code](../vs140/How-to--Enable-and-Disable-Automatic-Code-Analysis-for-Managed-Code.md)<br />-   [How to: Run Code Analysis Manually for Managed Code](../vs140/How-to--Run-Code-Analysis-Manually-for-Managed-Code.md)|  
|**Analyze code analysis results:** Code analysis warnings and errors are listed in the Code Analysis window. You can choose a warning or an error title to display additional information about the warning, and to display and highlight the source code line that fired the rule. You can choose the warning id to display detailed information in the MSDN Library that includes information and examples of how to resolve the issue.|-   [How to: View Managed Code Defects](../vs140/How-to--View-Managed-Code-Defects.md)<br />-   [Code Analysis for Managed Code Warnings](../vs140/Code-Analysis-for-Managed-Code-Warnings.md)<br />-   [Code Analysis Warnings for Managed Code by CheckId](../Topic/Code%20Analysis%20Warnings%20for%20Managed%20Code%20by%20CheckId.md)<br />-   [Anonymous Methods and Code Analysis](../vs140/Anonymous-Methods-and-Code-Analysis.md)|  
|**Integrate code analysis with your development life-cycle:** Check-in policies in [!INCLUDE[esprscc](../vs140/includes/esprscc_md.md)] enable development teams to make sure that all code check-ins meet a common set of code analysis standards. Creating a work item for a code analysis rule violation is simple procedure that you can perform in the Error List window.|-   [Enhancing Code Quality with Static Analysis Check-in Policies](../vs140/Enhancing-Code-Quality-with-Team-Project-Check-in-Policies.md)<br />-   [How to: Synchronize Code Project Rule Sets With Team Project Check-in Policy](../vs140/How-to--Synchronize-Code-Project-Rule-Sets-with-Team-Project-Check-in-Policy.md)<br />-   [How to: Create a Work Item for Managed Code Defect](../vs140/How-to--Create-a-Work-Item-for-a-Managed-Code-Defect.md)|