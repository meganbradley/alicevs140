---
title: "CImageList::Read"
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
ms.assetid: c56106b6-5dd5-4bd4-9f5d-e56f3486a99c
caps.latest.revision: 14
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CImageList::Read
Call this function to read an image list from an archive.  
  
## Syntax  
  
```  
  
      BOOL Read(  
   CArchive* pArchive   
);  
```  
  
#### Parameters  
 `pArchive`  
 A pointer to a `CArchive` object from which the image list is to be read.  
  
## Return Value  
 Nonzero if successful; otherwise 0.  
  
## Example  
 [!CODE [NVC_MFC_CImageList#18](../CodeSnippet/VS_Snippets_Cpp/NVC_MFC_CImageList#18)]  
  
## Requirements  
 **Header:** afxcmn.h  
  
## See Also  
 [CImageList Class](../vs140/CImageList-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [CImageList::Write](../vs140/CImageList--Write.md)