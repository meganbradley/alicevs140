---
title: "CMetaFileDC::Create"
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
ms.assetid: 44daa0fc-cabe-4d74-a5fc-c0810678cf8e
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CMetaFileDC::Create
Construct a `CMetaFileDC` object in two steps.  
  
## Syntax  
  
```  
  
      BOOL Create(  
   LPCTSTR lpszFilename = NULL   
);  
```  
  
#### Parameters  
 *lpszFilename*  
 Points to a null-terminated character string. Specifies the filename of the metafile to create. If *lpszFilename* is **NULL**, a new in-memory metafile is created.  
  
## Return Value  
 Nonzero if the function is successful; otherwise 0.  
  
## Remarks  
 First, call the constructor `CMetaFileDC`, then call **Create**, which creates the Windows metafile device context and attaches it to the `CMetaFileDC` object.  
  
## Requirements  
 **Header:** afxext.h  
  
## See Also  
 [CMetaFileDC Class](../vs140/CMetaFileDC-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CMetaFileDC::CMetaFileDC](../vs140/CMetaFileDC--CMetaFileDC.md)   
 [CDC::SetAttribDC](../vs140/CDC--SetAttribDC.md)   
 [CreateMetaFile](http://msdn.microsoft.com/library/windows/desktop/dd183506)