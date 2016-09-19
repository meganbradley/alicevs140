---
title: "Could not create output directory &#39;directory&#39;. &lt;reason&gt;"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - devlang-csharp
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: b4d1d19f-f582-49d0-a9a9-d3f4ce0a447b
caps.latest.revision: 11
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Could not create output directory &#39;directory&#39;. &lt;reason&gt;
The project system could not create a project directory.  
  
 The project system will attempt to create all output directories as soon as the project is opened. The following is a list of the output directories created by the project system:  
  
 *projectfolder*\obj\\`configname`  
 A temporary configuration-specific output directory.  
  
 *projectfolder*\obj\\`configname`\temp  
 Working area used by the compiler.  
  
 *projectfolder*\obj\\`configname`\temppe  
 Temporary assemblies used by designers at design-time are created here.  
  
 outputdir  
 The directory specified by the Output Path property. See [Build Pane, Project Designer (C#)](../Topic/Build%20Page,%20Project%20Designer%20\(C%23\).md) for more information.  
  
 The most common reason for failing to create one of the directories under the obj folder is exceeding the MAX_PATH limit for directory names.  
  
 Less common reasons will include permission denied and out of disk space.  
  
 **To correct this error**  
  
-   If the path is too long, change the project location or shorten the name of the project configuration.  
  
     The build process will fail if this error occurs.  
  
## See Also  
 [NIB How to: Modify Project Properties and Configuration Settings](assetId:///e7184bc5-2f2b-4b4f-aa9a-3ecfcbc48b67)