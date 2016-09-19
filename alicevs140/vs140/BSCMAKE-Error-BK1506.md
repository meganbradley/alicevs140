---
title: "BSCMAKE Error BK1506"
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
ms.assetid: f51f8cea-f8fc-4323-bcf2-b7bd119792ee
caps.latest.revision: 8
translation.priority.ht: 
  - de-de
  - ja-jp
---
# BSCMAKE Error BK1506
cannot open file 'filename' [: reason]  
  
 BSCMAKE cannot open the file.  
  
### To fix by checking the following possible causes  
  
1.  File locked by another process. If `reason` says **Permission denied**, the browser may be using the file. Close the Browse window and retry the build.  
  
2.  A full disk.  
  
3.  A hardware error.  
  
4.  The specified output file has the same name as an existing subdirectory.