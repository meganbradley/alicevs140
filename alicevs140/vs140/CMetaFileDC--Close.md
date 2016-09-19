---
title: "CMetaFileDC::Close"
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
ms.assetid: 8ff8095a-01e5-40fa-8f82-719ce2c19d5b
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMetaFileDC::Close
Closes the metafile device context and creates a Windows metafile handle that can be used to play the metafile by using the [CDC::PlayMetaFile](../vs140/CDC--PlayMetaFile.md) member function.  
  
## Syntax  
  
```  
  
HMETAFILE Close( );  
```  
  
## Return Value  
 A valid **HMETAFILE** if the function is successful; otherwise **NULL**.  
  
## Remarks  
 The Windows metafile handle can also be used to manipulate the metafile with Windows functions such as [CopyMetaFile](http://msdn.microsoft.com/library/windows/desktop/dd183480).  
  
 Delete the metafile after use by calling the Windows [DeleteMetaFile](http://msdn.microsoft.com/library/windows/desktop/dd183537) function.  
  
## Requirements  
 **Header:** afxext.h  
  
## See Also  
 [CMetaFileDC Class](../vs140/CMetaFileDC-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CDC::PlayMetaFile](../vs140/CDC--PlayMetaFile.md)   
 [CloseMetaFile](http://msdn.microsoft.com/library/windows/desktop/dd183445)   
 [CopyMetaFile](http://msdn.microsoft.com/library/windows/desktop/dd183480)   
 [DeleteMetaFile](http://msdn.microsoft.com/library/windows/desktop/dd183537)