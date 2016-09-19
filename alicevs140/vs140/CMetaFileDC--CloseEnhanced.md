---
title: "CMetaFileDC::CloseEnhanced"
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
ms.assetid: 444fe3c5-9682-422e-afbf-15d08dba6fab
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMetaFileDC::CloseEnhanced
Closes an enhanced-metafile device context and returns a handle that identifies an enhanced-format metafile.  
  
## Syntax  
  
```  
  
HENHMETAFILE CloseEnhanced( );  
```  
  
## Return Value  
 A handle of an enhanced metafile, if successful; otherwise **NULL**.  
  
## Remarks  
 An application can use the enhanced-metafile handle returned by this function to perform the following tasks:  
  
-   Display a picture stored in an enhanced metafile  
  
-   Create copies of the enhanced metafile  
  
-   Enumerate, edit, or copy individual records in the enhanced metafile  
  
-   Retrieve an optional description of the metafile contents from the enhanced-metafile header  
  
-   Retrieve a copy of the enhanced-metafile header  
  
-   Retrieve a binary copy of the enhanced metafile  
  
-   Enumerate the colors in the optional palette  
  
-   Convert an enhanced-format metafile into a Windows-format metafile  
  
 When the application no longer needs the enhanced metafile handle, it should release the handle by calling the Win32 **DeleteEnhMetaFile** function.  
  
## Requirements  
 **Header:** afxext.h  
  
## See Also  
 [CMetaFileDC Class](../vs140/CMetaFileDC-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CDC::PlayMetaFile](../vs140/CDC--PlayMetaFile.md)   
 [CMetaFileDC::CreateEnhanced](../vs140/CMetaFileDC--CreateEnhanced.md)   
 [DeleteEnhMetaFile](http://msdn.microsoft.com/library/windows/desktop/dd183534)