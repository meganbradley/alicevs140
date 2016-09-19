---
title: "Project Build Error PRJ0050"
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
ms.assetid: ceef3b37-0acf-4abd-ac62-aa830b4fa145
caps.latest.revision: 6
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Project Build Error PRJ0050
Failed to register output. Please ensure you have the appropriate permissions to modify the registry.  
  
 The Visual C++ build system was not able to register the output of the build (dll or .exe). You need to be logged on as an administrator to modify the registry.  
  
 If you are building a .dll, you can try to register the .dll manually using regsvr32.exe, this should display information about why the build failed.  
  
 If you are not building a .dll, look at the build log for the command that causes an error.