---
title: "SccEnumChangedFiles Function"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - vs-ide-sdk
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 76cac510-107b-4c1a-ba60-9c39b6db2e71
caps.latest.revision: 14
translation.priority.mt: 
  - de-de
  - ja-jp
---
# SccEnumChangedFiles Function
Given a list of local files, this function determines which files are different from the corresponding versions in the source code control database.  
  
## Syntax  
  
```cpp  
SCCRTN SccEnumChangedFiles(  
   LPVOID  pContext,  
   HWND    hWnd,  
   LONG    cFiles,  
   LPCSTR* lpFileNames,  
   LONG*   plIsFileDifferent  
);  
```  
  
#### Parameters  
 pContext  
 [in] The source control plug-in context pointer.  
  
 hWnd  
 [in] A handle to the IDE window that the source control plug-in can use as a parent for any dialog boxes that it provides.  
  
 cFiles  
 [in] Number of file names specified in the `lpFileNames` array. Also specifies size of `plIsFileDifferent` array.  
  
 lpFileNames  
 [in] Array of local file names to check.  
  
 plIsFileDifferent  
 [in, out] Array of values indicating the difference status of each file (array must have at least `cFiles` entries). Nonzero means that the file is different.  
  
## Return Value  
 The source control plug-in implementation of this function is expected to return one of the following values:  
  
|Value|Description|  
|-----------|-----------------|  
|SCC_OK|Operation completed successfully.|  
|SCC_UNSPECIFIEDERROR|Generic error.|  
  
## See Also  
 [Source Control Plug-in API Functions](../vs140/Source-Control-Plug-in-API-Functions.md)