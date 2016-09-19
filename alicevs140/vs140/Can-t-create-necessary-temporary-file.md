---
title: "Can&#39;t create necessary temporary file"
ms.custom: na
ms.date: 09/19/2016
ms.devlang: 
  - VB
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - devlang-visual-basic
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 53617b5b-eb06-4188-b4c2-8607cb9fbc79
caps.latest.revision: 8
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Can&#39;t create necessary temporary file
Either the drive is full that contains the directory specified by the TEMP environment variable, or the TEMP environment variable specifies an invalid or read-only drive or directory.  
  
### To correct this error  
  
1.  Delete files from the drive, if full.  
  
2.  Specify a different drive in the TEMP environment variable.  
  
3.  Specify a valid drive for the TEMP environment variable.  
  
4.  Remove the read-only restriction from the currently specified drive or directory.  
  
## See Also  
 [Types of Errors](../vs140/Error-Types--Visual-Basic-.md)