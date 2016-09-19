---
title: "Project Build Error PRJ0009"
ms.custom: na
ms.date: 09/18/2016
ms.devlang: 
  - C++
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - devlang-cpp
ms.tgt_pltfrm: na
ms.topic: error-reference
ms.assetid: 89291778-cda4-495d-983f-ddcc06dfc98b
caps.latest.revision: 8
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Project Build Error PRJ0009
Build log could not be opened for writing.  
  
 **Make sure that the file is not open by another process and is not write-protected.**  
  
 After setting the **Build Logging** property to **Yes** and performing a build or rebuild, Visual C++ was unable to open the build log in exclusive mode.  
  
 Inspect the **Build Logging** setting by opening the **Options** dialog box (on the **Tools** menu, click **Options** command) and then selecting **VC++ Build** in the **Projects** folder. The build file is called BuildLog.htm and is written to the intermediate directory $(IntDir).  
  
 Possible reasons for this error:  
  
-   You are running two processes of Visual C++ and trying to build the same configuration of the same project in both simultaneously.  
  
-   The build log file is opened in a process that locks the file.  
  
-   The user does not have permission to create a file.  
  
-   The current user does not have write access to the file BuildLog.htm.