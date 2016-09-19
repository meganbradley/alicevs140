---
title: "SccPopulateDirList Function"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - vs-ide-sdk
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: dfff634b-b155-498b-a356-6eb252ac4fad
caps.latest.revision: 13
translation.priority.mt: 
  - de-de
  - ja-jp
---
# SccPopulateDirList Function
This function determines which directories and (optionally) files are stored in source control, given a list of directories to examine.  
  
## Syntax  
  
```cpp  
SCCRTN SccPopulateDirList(  
   LPVOID        pContext,  
   LONG          nDirs,  
   LPCSTR*       lpDirPaths,  
   POPDIRLISTFUNCpfnPopulate,  
   LPVOID        pvCallerData,  
   LONG          fOptions  
);  
```  
  
#### Parameters  
 pContext  
 [in] The source control plug-in context pointer.  
  
 nDirs  
 [in] Number of directory paths in the `lpDirPaths` array.  
  
 lpDirPaths  
 [in] Array of directory paths to examine.  
  
 pfnPopulate  
 [in] Callback function to call for each directory path and (optionally) filename in `lpDirPaths` (see [POPDIRLISTFUNC](../vs140/POPDIRLISTFUNC.md) for details).  
  
 pvCallerData  
 [in] Value that is to be passed unchanged to the callback function.  
  
 fOptions  
 [in] A combination of values that control how the directories are processed (see the "PopulateDirList flags" section of [Bitflags Used by Specific Commands](../vs140/Bitflags-Used-by-Specific-Commands.md) for possible values).  
  
## Return Value  
 The source control plug-in implementation of this function is expected to return one of the following values:  
  
|Value|Description|  
|-----------|-----------------|  
|SCC_OK|Successfully completed the operation.|  
|SCC_E_UNKNOWNERROR|An error occurred.|  
  
## Remarks  
 Only those directories and (optionally) file names that are actually in the source control repository are passed to the callback function.  
  
## See Also  
 [Source Control Plug-in API Functions](../vs140/Source-Control-Plug-in-API-Functions.md)   
 [Bitflags Used by Specific Commands](../vs140/Bitflags-Used-by-Specific-Commands.md)   
 [POPDIRLISTFUNC](../vs140/POPDIRLISTFUNC.md)   
 [Error Codes](../vs140/Error-Codes.md)