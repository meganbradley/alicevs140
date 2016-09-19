---
title: "File Attribute Constants"
ms.custom: na
ms.date: 09/19/2016
ms.devlang: 
  - C++
  - C
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - devlang-cpp
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 8dc8ccb9-99f5-446b-876c-7ebecc2f764f
caps.latest.revision: 8
translation.priority.ht: 
  - de-de
  - ja-jp
---
# File Attribute Constants
## Syntax  
  
```  
  
#include <io.h>  
```  
  
## Remarks  
 These constants specify the current attributes of the file or directory specified by the function.  
  
 The attributes are represented by the following manifest constants:  
  
 `_A_ARCH`  
 Archive. Set whenever the file is changed, and cleared by the BACKUP command. Value: 0x20  
  
 `_A_HIDDEN`  
 Hidden file. Not normally seen with the DIR command, unless the /AH option is used. Returns information about normal files as well as files with this attribute. Value: 0x02  
  
 `_A_NORMAL`  
 Normal. File can be read or written to without restriction. Value: 0x00  
  
 `_A_RDONLY`  
 Read-only. File cannot be opened for writing, and a file with the same name cannot be created. Value: 0x01  
  
 `_A_SUBDIR`  
 Subdirectory. Value: 0x10  
  
 `_A_SYSTEM`  
 System file. Not normally seen with the DIR command, unless the /AS option is used. Value: 0x04  
  
 Multiple constants can be combined with the OR operator (&#124;).  
  
## See Also  
 [Filename Search Functions](../vs140/Filename-Search-Functions.md)   
 [Global Constants](../vs140/Global-Constants.md)