---
title: "Directory Status Code Enumerator"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - vs-ide-sdk
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 616026b5-f529-40ef-90c1-1836e116d797
caps.latest.revision: 15
translation.priority.mt: 
  - de-de
  - ja-jp
---
# Directory Status Code Enumerator
The `SccDirStatus` enumerator contains named constant values that specify the state of a directory in the source control system. This enumeration is used by the [SccDirQueryInfo Function](../vs140/SccDirQueryInfo-Function.md). This was introduced in version 1.2 of the Source Control Plug-in API.  
  
## Syntax  
  
```  
enum SccDirStatus {  
   SCC_DIRSTATUS_INVALID       = -1L,  
   SCC_DIRSTATUS_NOTCONTROLLED = 0x0000L,  
   SCC_DIRSTATUS_CONTROLLED    = 0x0001L,  
   SCC_DIRSTATUS_EMPTYPROJ     = 0x0002L  
};  
```  
  
## Members  
 SCC_DIRSTATUS_INVALID  
 Status could not be obtained; do not rely on it.  
  
 SCC_DIRSTATUS_NOTCONTROLLED  
 Directory is not under source control.  
  
 SCC_DIRSTATUS_CONTROLLED  
 Directory is under source control.  
  
 SCC_DIRSTATUS_EMPTYPROJ  
 Project corresponding to this directory is empty.  
  
## See Also  
 [Source Control Plug-ins](../vs140/Source-Control-Plug-ins.md)   
 [SccDirQueryInfo Function](../vs140/SccDirQueryInfo-Function.md)