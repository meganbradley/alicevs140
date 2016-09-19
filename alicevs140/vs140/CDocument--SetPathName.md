---
title: "CDocument::SetPathName"
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
ms.topic: reference
ms.assetid: 6568fb06-e34b-4307-a0cc-af7352db2ef4
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CDocument::SetPathName
Call this function to specify the fully qualified path of the document's disk file.  
  
## Syntax  
  
```  
  
      virtual void SetPathName(  
   LPCTSTR lpszPathName,  
   BOOL bAddToMRU = TRUE   
);  
```  
  
#### Parameters  
 `lpszPathName`  
 Points to the string to be used as the path for the document.  
  
 `bAddToMRU`  
 Determines whether the filename is added to the most recently used (MRU) file list. If **TRUE,** the filename is added; if **FALSE**, it is not added.  
  
## Remarks  
 Depending on the value of `bAddToMRU` the path is added, or not added, to the MRU list maintained by the application. Note that some documents are not associated with a disk file. Call this function only if you are overriding the default implementation for opening and saving files used by the framework.  
  
## Requirements  
 **Header:** afxwin.h  
  
## See Also  
 [CDocument Class](../vs140/CDocument-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CDocument::GetPathName](../vs140/CDocument--GetPathName.md)   
 [CWinApp::AddToRecentFileList](../vs140/CWinApp--AddToRecentFileList.md)