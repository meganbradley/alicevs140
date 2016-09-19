---
title: "The user options settings file for this project is missing the &#39;section&#39; section"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - devlang-csharp
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 576070f5-76b6-46e4-8aba-83442521027f
caps.latest.revision: 9
translation.priority.ht: 
  - de-de
  - ja-jp
---
# The user options settings file for this project is missing the &#39;section&#39; section
The Build node is missing from the.vbproj.user or .csproj.user file.  
  
 The Build section encompasses debugging settings. If this section is missing, your debugging settings will not be loaded and will take on default values.  
  
 The situation is most likely caused by editing the project file by hand.  
  
 The project system will automatically rewrite the per-user project file when the project is closed.  
  
 This is an informational warning.  
  
## See Also  
 [Project Files](../vs140/Project-Files.md)   
 [NIB: Project Properties (Visual Studio)](assetId:///eb4c97ed-f667-4850-98d0-6e2a4d21bbca)