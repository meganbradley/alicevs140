---
title: "SccBackgroundGet Function"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - vs-ide-sdk
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 69817e52-b9ac-4f4d-820b-2cc9c384f0dc
caps.latest.revision: 15
translation.priority.mt: 
  - de-de
  - ja-jp
---
# SccBackgroundGet Function
This function retrieves from source control each of the specified files with no user interaction.  
  
## Syntax  
  
```cpp  
SCCRTN SccBackgroundGet(  
   LPVOID  pContext,  
   LONG    nFiles,  
   LPCSTR* lpFileNames,  
   LONG    dwFlags,  
   LONG    dwBackgroundOperationID  
);  
```  
  
#### Parameters  
 pContext  
 [in] The source control plug-in context pointer.  
  
 nFiles  
 [in] Number of files specified in the `lpFileNames` array.  
  
 lpFileNames  
 [in, out] Array of names of files to be retrieved.  
  
> [!NOTE]
>  The names must be fully qualified local filenames.  
  
 dwFlags  
 [in] Command flags (`SCC_GET_ALL`, `SCC_GET_RECURSIVE`).  
  
 dwBackgroundOperationID  
 [in] A unique value associated with this operation.  
  
## Return Value  
 The source control plug-in implementation of this function is expected to return one of the following values:  
  
|Value|Description|  
|-----------|-----------------|  
|SCC_OK|Operation completed successfully.|  
|SCC_E_BACKGROUNDGETINPROGRESS|A background retrieval is already in progress (the source control plug-in should return this only if it does not support simultaneous batch operations).|  
|SCC_I_OPERATIONCANCELED|Operation was canceled before being completed.|  
  
## Remarks  
 This function is always called on a thread different from the one that loaded the source control plug-in. This function is not expected to return until it is done; however, it can be called multiple times with multiple lists of files, all at the same time.  
  
 The use of the `dwFlags` argument is the same as the [SccGet Function](../vs140/SccGet-Function.md).  
  
## See Also  
 [Source Control Plug-in API Functions](../vs140/Source-Control-Plug-in-API-Functions.md)   
 [SccGet Function](../vs140/SccGet-Function.md)