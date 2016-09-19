---
title: "BSCMAKE Warning BK4502"
ms.custom: na
ms.date: 09/19/2016
ms.devlang: 
  - C++
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - devlang-cpp
ms.tgt_pltfrm: na
ms.topic: error-reference
ms.assetid: ee412ec8-df03-4cdb-91ee-5d609ded8691
caps.latest.revision: 9
translation.priority.ht: 
  - de-de
  - ja-jp
---
# BSCMAKE Warning BK4502
truncated .SBR file 'filename' not in filename  
  
 A zero-length .sbr file that was not originally part of the .bsc file was specified during an update.  
  
### To fix by checking the following possible causes  
  
1.  Wrong filename specified.  
  
2.  File deleted. (Error [BK1513](../vs140/BSCMAKE-Error-BK1513.md) results.)  
  
3.  File corrupted, requiring BSCMAKE to do a full build.