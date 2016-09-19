---
title: "CDC::AddMetaFileComment"
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
ms.assetid: 93f376b3-5c84-4221-8675-7f39855e5402
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CDC::AddMetaFileComment
Copies the comment from a buffer into a specified enhanced-format metafile.  
  
## Syntax  
  
```  
  
      BOOL AddMetaFileComment(  
   UINT nDataSize,  
   const BYTE* pCommentData   
);  
```  
  
#### Parameters  
 *nDataSize*  
 Specifies the length of the comment buffer, in bytes.  
  
 *pCommentData*  
 Points to the buffer that contains the comment.  
  
## Return Value  
 Nonzero if the function is successful; otherwise 0.  
  
## Remarks  
 A comment may include any private information — for example, the source of the picture and the date it was created. A comment should begin with an application signature, followed by the data. Comments should not contain position-specific data. Position-specific data specifies the location of a record, and it should not be included because one metafile may be embedded within another metafile. This function can only be used with enhanced metafiles.  
  
## Requirements  
 **Header:** afxwin.h  
  
## See Also  
 [CDC Class](../vs140/CDC-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CMetaFileDC::CreateEnhanced](../vs140/CMetaFileDC--CreateEnhanced.md)   
 [GdiComment](http://msdn.microsoft.com/library/windows/desktop/dd144843)