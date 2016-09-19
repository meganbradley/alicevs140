---
title: "POPDIRLISTFUNC"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - vs-ide-sdk
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 0ee90fd2-5467-4154-ab4c-7eb02ac3a14c
caps.latest.revision: 16
translation.priority.mt: 
  - de-de
  - ja-jp
---
# POPDIRLISTFUNC
This is a callback function given to the [SccPopulateDirList](../vs140/SccPopulateDirList-Function.md) function to update a collection of directories and (optionally) file names to find out which are under source control.  
  
 The `POPDIRLISTFUNC` callback should be called only for those directories and file names (in the list given to the `SccPopulateDirList` function) that are actually under source control.  
  
## Signature  
  
```cpp#  
typedef BOOL (*POPDIRLISTFUNC)(  
   LPVOID pvCallerData,  
   BOOL bFolder,  
   LPCSTR lpDirectoryOrFileName  
);  
```  
  
## Parameters  
 pvCallerData  
 [in] User value given to [SccPopulateDirList](../vs140/SccPopulateDirList-Function.md).  
  
 bFolder  
 [in] `TRUE` if the name in `lpDirectoryOrFileName` is a directory; otherwise the name is a file name.  
  
 lpDirectoryOrFileName  
 [in] Full local path to a directory or file name that is under source code control.  
  
## Return Value  
 The IDE returns an appropriate error code:  
  
|Value|Description|  
|-----------|-----------------|  
|SCC_OK|Continue processing.|  
|SCC_I_OPERATIONCANCELED|Stop processing.|  
|SCC_E_xxx|Any appropriate source control error should stop processing.|  
  
## Remarks  
 If the `fOptions` parameter of the `SccPopulateDirList` function contains the `SCC_PDL_INCLUDEFILES` flag, then the list will possibly contain file names as well as directory names.  
  
## See Also  
 [Callback Functions Implemented by the IDE](../vs140/Callback-Functions-Implemented-by-the-IDE.md)   
 [SccPopulateDirList](../vs140/SccPopulateDirList-Function.md)   
 [Error Codes](../vs140/Error-Codes.md)